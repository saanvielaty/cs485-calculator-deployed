# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
## API Configuration

Frontend API calls are configured with Vite environment variables.

Use one of these options:

- `VITE_API_CALCULATE_URL`: full calculator endpoint URL.
	- Example: `https://1e2jckpbb9.execute-api.us-east-2.amazonaws.com/calculator`
- `VITE_API_BASE_URL`: base URL only; app will call `${VITE_API_BASE_URL}/calculate`.

For your current AWS setup (API Gateway POST method URL), set:

- `VITE_API_CALCULATE_URL=https://1e2jckpbb9.execute-api.us-east-2.amazonaws.com/calculator`

On AWS Amplify:

1. Open Amplify app -> Hosting -> Environment variables.
2. Add `VITE_API_CALCULATE_URL` with the value above.
3. Redeploy the frontend.