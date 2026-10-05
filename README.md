# admin

The restricted administration application at `admin.rsl-commerce.test`, for the people
who run the store.

## Responsibilities

- Product and inventory management
- Order management, payment inspection and refunds
- Subscription and customer management
- Marketing: running campaigns and promotions
- Role management for staff, for example Administrator, Support Agent, Catalog Manager, Finance User
  and Read Only
- System activity, audit logs and operational dashboards
- Live alerts: new orders, failed payments, finished background jobs, low inventory and past-due
  subscriptions

## Does not own

- Authorization decisions. The backend enforces every permission; the admin only reflects them.
- Components and design tokens. Those come from the design system.
- Any direct access to the database, cache or message broker.

## Works with

- **backend.** The admin uses the API through the generated SDK, and gets live updates over
  WebSocket.
- **design-system.** It supplies the components, tokens and shared tooling.

## Git hooks

Run `.githooks/setup` once after cloning. It turns on the committed hooks, which use
[git-secrets](https://github.com/awslabs/git-secrets#installing-git-secrets) to refuse any commit
that contains a secret.

## Status

Planning. No code yet.

## License

[MIT](LICENSE)
