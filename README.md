# apidoc

This is a small example of how to use apidoc in docker

## Installation

Create a build folder in root.

```bash
mkdir build
```

Use the disgusting command for docker to build the necessary image

```bash
docker build -t apidoc/apidoc .
```

## Usage


Add the mock code of the api. You can see more information on the official page of apidoc

```javascript
/**
 * @api {get} /user/:id Read data of a User
 * @apiVersion 0.3.0
 * @apiName GetUser
 * @apiGroup User
 * @apiPermission admin
 */
```


Run docker to build documentation
```bash
docker run -it --rm -v "$(PWD):/apidoc" simnare/apidocjs -i ./src -o ./build/doc -v
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
