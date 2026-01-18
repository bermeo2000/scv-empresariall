
# Decisiones de Workflow - SCV Empresarial

## ¿Cuándo usamos rebase?
- Para limpiar commits locales antes de hacer push al repositorio remoto.
- Para mantener un historial lineal en ramas de feature.
- Ejemplo: Usamos `git rebase -i` para combinar varios commits experimentales en uno solo antes de integrarlos a main.

## ¿Cuándo usamos merge?
- Para integrar ramas de feature completadas a main.
- Cuando queremos preservar el contexto de cuándo se unió la rama.
- Ejemplo: Merge de `feature/login` a `main` para añadir funcionalidades finales.

## ¿Cuándo usamos cherry-pick?
- Para aplicar commits selectivos listos para producción sin traer código incompleto o experimental.
- Ejemplo: Cherry-pick de la función B (`feat: add function B`) desde `feature/experimental` a `main`, dejando las funciones A y C experimentales fuera.

## Lecciones aprendidas en la Fase 2
- El rebase es útil para limpiar y organizar commits, pero hay que evitarlo en ramas compartidas para no romper el historial de otros.
- El merge preserva el historial completo y ayuda a ver cuándo se integraron cambios importantes.
- El cherry-pick permite aplicar hotfixes o funcionalidades listas sin traer código incompleto.
- Siempre revisar conflictos cuidadosamente; los conflictos de tipo “modify/delete” pueden aparecer si un archivo existe en un commit pero fue eliminado en main.
- Mantener commits claros y descriptivos facilita la gestión del historial y la colaboración.