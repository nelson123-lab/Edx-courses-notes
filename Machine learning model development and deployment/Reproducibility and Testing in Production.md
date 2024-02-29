## Reproducibility in Machine learning production
- Training should be reproducible; without reproducible training mechanisms, it reduces the effectiveness of canary release.
- Every model specification undergoes a code review and is checked into a repository.
- Models can be quickly and safely rolled back to a previous serving version.
- Automate the end-to-end pipeline for easy reproducibility.

## Testing Machine learning models for production.
- pytest is usually used for testing.
- All input feature code is tested.
- Model specification code should be unit-tested.
- Models are tested via a shadow/canary process before they enter production serving environments.

### Shadow deployment.
- When we collect the model predictions in production for analysis and we don't serve those predictions to customers until we are satisfied with the results.

### Canary deployment
- When we serve the model predictions to a limited customer group.
