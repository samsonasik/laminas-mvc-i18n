# Migration: laminas-mvc v2 to laminas-mvc-i18n

laminas-mvc-i18n ports all i18n integration functionality from the laminas-mvc v2
release to a single component. As such, a number of classes were renamed that
could potentially impact end-users.

## TranslatorAwareTreeRouteStack

`Laminas\Mvc\Router\Http\TranslatorAwareTreeRouteStack` was renamed to
`Laminas\Mvc\I18n\Router\TranslatorAwareTreeRouteStack`. It functions exactly as
the original, however, including accepting the same configuration.

## TranslatorServiceFactory

`Laminas\Mvc\Service\TranslatorServiceFactory` was renamed to
`Laminas\Mvc\I18n\TranslatorFactory`. Behavior remains the same.

## Exceptions thrown by the MVC translator

In v2 releases, `Laminas\Mvc\I18n\Translator` would throw exceptions from the
`Laminas\Mvc\Exception` namespace. It now throws exceptions from the new
`Laminas\Mvc\I18n\Exception` namespace.
