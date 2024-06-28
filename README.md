# Default template for CandyMint

[CandyMint][1] is a platform for creating and minting NFTs. This repository contains the default template to help creators build their own asset repository.

## Usage

1. Click `Use this template` to create your own repository
1. Upload images in the `image` directory
1. Update the `layouts.yaml` file
1. Connect your repository with your collection created in the CandyMint platform

## Template Structure

```text
image
├── item1.png
├── item2.png
├── ...
README.md
layouts.yaml
```

- `image` contains the images of the NFT items.
- `README.md` is the README file of the repository.
- `layouts.yaml` is the configuration file of the NFT items.

## Anatomy

```yaml
template: default             # template name, DO NOT change
engine: 0.1.0                 # engine version, DO NOT change
config:
  mime: image/png             # image mime type
  size:
    width: 64                 # image width
    height: 64                # image height
    # ...                     # other properties used internally, DO NOT change
items:
  - token_id: 1               # token id, should be unique and sequential
    image_uri: 'item_01.png'   # file name of the item, relative to the image directory
    token_trait:              # token traits
      - trait_type: letter
        display_type: string
        value: a
      # other traits...
  # other items...
```

**Caveats:**

- The `image` directory **MUST** contain only images.
- The `layouts.yaml` file **MUST** be valid YAML.
- Since the CandyMint platform supports multiple versions, when you adding new images and updating the `layouts.yaml`, **DO NOT** change existing token_id or the order of items.
- To enable [on-chain storage][6], make sure your image file is no larger than 50KB.

## TODO

- [ ] Add a license

## Other Templates

- [Default Template](https://github.com/originpoint-at/nft-template-default)
- [SVG Composite Template](https://github.com/originpoint-at/nft-template-svg-composite)
- [PNG Composite Template](https://github.com/originpoint-at/nft-template-png-composite)

## Relative Links

- [CandyMint][1]
- [CandyMint Testnet][2]
- [CandyMint Docs][3]
- [PNG Composite Tool][5]
- [Discord][4]
- Twitter
- Telegram

[1]: https://candymint.io
[2]: https://testnet.candymint.io
[3]: https://docs.candymint.io
[4]: https://discord.gg/DyP5Vxw5VB
[5]: https://candymint.io/tools/png-composite-tool
[6]: https://docs.candymint.io/introduction#what-is-on-chain-storage
