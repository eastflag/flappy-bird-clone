git clone https://github.com/Jerga99/phaser-webpack-boilerplate
mv phaser-webpack-boilerplate flappy-bird-clone
cd flappy-bird-clone
npm run dev

에러 발생시 webpack.common.js 수정
```json
    new CopyPlugin({
      patterns: [
        {
          from: path.resolve(__dirname, 'assets/**/*'),
          to: path.resolve(__dirname, 'build')
        }
      ],
    })
```

```json
    new CopyPlugin({
  patterns: [
    {
      from: path.resolve(__dirname, 'assets'),
      to: path.resolve(__dirname, 'build/assets')
    }
  ],
})
```

