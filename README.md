## Metaverse test

- [Sonny Sangha - Metaverse reactjs Challenge](https://www.youtube.com/watch?v=3NpZ05sDTQ4)

## init

```sh
> npx create-next-app --example with-tailwindcss
```

## Image

```js
import Image from 'next/image';

const Component = () => {
	return <Image src="https://links.papareact.com/55n" />;
};

export default Component;
```

- next.config.js : host prop connect

# Implementing Moralis

## [react-moralis](https://docs.moralis.io/moralis-server/tools/react-moralis)

```sh
> npm install react-moralis
```

```js
// _app.js
import '../styles/globals.css';
import { MoralisProvider } from 'react-moralis';

function MyApp({ Component, pageProps }) {
	return (
		<MoralisProvider appId="xxxxxxxx" serverUrl="xxxxxxxx">
			<Component {...pageProps} />
		</MoralisProvider>
	);
}

export default MyApp;
```

- 보안을 위해 local영역에서 다룰때는 .env 이용

```js
// .env.local
NEXT_PUBLIC_APP_ID = "xxxxxxxx"
NEXT_PUBLIC_SERVER_URL =  "xxxxxxxx"


// _app.js
<MoralisProvider
	appId={process.env.NEXT_PUBLIC_APP_ID}
	serverUrl={process.env.NEXT_PUBLIC_SERVER_URL}
>
	<Component {...pageProps} />
</MoralisProvider>
```

```sh
> npm i @walletconnect/web3-provider
```
