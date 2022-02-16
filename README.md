![alt text](https://raw.githubusercontent.com/ossgroupp/react-content-transformer/HEAD/media/logo.png 'Pie with slice')

# React OSSPIM Content Transformer

Transform OSSPIM rich text json to React html components. Makes it easy to build React Commerce solutions with [Product Information Management](https://ossgroup.com/product/product-information-management) powered by [OSSPIM](https://ossgroup.com) that enable [Fast Ecommerce API](https://ossgroup.com/product/graphql-commerce-api).

## In Typescript

```
import { ContentTransformer, NodeContent, Overrides, NodeProps } from '@osspim/react-content-transformer';

const overrides: Overrides = {
  link: (props: NodeProps) => (
    <a href={props.metadata?.href}>
      <NodeContent {...props} />
    </a>
  ),
};

<ContentTransformer json={richTextJson} overrides={overrides} />
```

## In Javascript

```
import { ContentTransformer, NodeContent } from '@osspim/react-content-transformer';

const overrides = {
  link: props => <a href={props.metadata.href}><NodeContent {...props} /></a>
};

<ContentTransformer json={richTextJson} overrides={overrides} />
```
# react-content-transformer
