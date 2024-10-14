# Encabezado de nivel 1
## Encabezado de nivel 2
### Encabezado de nivel 3
Esto es mi primer contenido en Markdown
## Imagen en Markdown
![Ul selfie con los amigos](https://i.pinimg.com/enabled_lo/564x/c7/93/f9/c793f9601562253642da8dda96f147e9.jpg)
## Añadiendo código en Markdown
Esto es un código de R inserado en markdown
``` R
lbls_action <- c("Fines", "Valores", "Afectiva", "Tradicional", "No contenciosa")
lbls_action_abrv <- c("RF","RV","AF","TR","NC")
#creación de datos para gráficos
# contSubjects
cntSubj <- db_fa %>%
    select(action_list) %>%
    unnest(action_list) %>%
    count(action_list) %>%
    mutate(action_list = factor(action_list, levels = lbls_action)) %>%
    mutate(prop = round(n / 174, digits = 2))
```
