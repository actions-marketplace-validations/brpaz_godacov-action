# Godacov Action

> GitHub Action for [godacov](https://github.com/schrej/godacov), a command-line tool to publish test coverage reports generated with `go test` to [Codacy](https://codacy.com).

[![GitHub Action](https://img.shields.io/badge/GitHub-Action-blue?style=for-the-badge)](https://github.com/features/actions)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![GitHub Actions](https://github.com/brpaz/godacov-action/workflows/Test/badge.svg?style=for-the-badge)](https://github.com/brpaz/godacov-action/actions)

## Usage

```yml
steps:
    uses: brpaz/godacov-action@v1
    with:
        reportPath: 'path/to/cover/file'
        codacyToken: ${{ secrets.CODACY_TOKEN }}
        commitId: ${{ github.sha }}
```

## Inputs

### `reportPath`

**Required** The path to the report file generated by `go test`. Default `"cover.out"`.

### `codacyToken`

**Required** The the token to authenticate into Codacy API.

### `commitId`

**Required** The identifier for the commit. you can use `${{ github.sha }}` to get the current commit hash.


## 🤝 Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Author

👤 **Bruno Paz**

* Website : [https://github.com/brpaz](https://github.com/brpaz)
* Github: [@brpaz](https://github.com/brpaz)

## 📝 License

Copyright © 2019 [Bruno Paz](https://github.com/brpaz).

This project is [MIT](LICENSE) licensed.
