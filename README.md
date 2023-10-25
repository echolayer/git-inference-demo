# ECHOLAYER PLAY INFERENCE

## Requirements
Node Version: `v20.6.1`

### Testing Inference Library
`node index.js <local_absolute_path_of_repo_to_be_analyzed> <number_of_modules_to_be_analyzed>`

For example: `node index.js /home/user/api-repo 10`

`local_absolute_path_of_repo_to_be_analyzed`: The absolute path of the repo to be analyzed. The repo should be cloned locally. (You may clone a repository bare using `git clone --bare <repo_url>`)

`number_of_modules_to_be_analyzed`: The number of commits to be analyzed (If left empty the script will attempt to analyze all commits in the repo)

Tip: If the process is taking too long, cancel the process and reduce the number of commits analyzed (`number_of_modules_to_be_analyzed`) which is 2500 by default.

### Example Output
```
{
// The name is the location where we believe a module exists
  name: 'src/modules/auth', 
  typeId: undefined,
  metadata: {
	// They keys are nouns that we believe could describe your module
    keywords: Map(11) {
      'auth' => 9,
      'github' => 8,
      'gitlab' => 7,
      'use' => 6,
      'base' => 6,
      'org' => 3,
      'user' => 2,
      'oauth' => 1,
      'config' => 1,
      'path' => 1,
      'work' => 1
    }
  },
  links: [
    {
      name: 'git',
      url: 'https://github.com/usecodex/echolayer-api/tree/development/src/modules/auth'
    }
  ]
}
```
