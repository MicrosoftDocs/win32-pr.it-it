---
title: importlib (attributo)
description: La direttiva \ importlib\ rende disponibili i tipi già compilati in un'altra libreria dei tipi per la libreria dei tipi creata.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- Attributo importlib MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d5c4b19800f92e3080d3fb435ddd20d62e4b6fe76986869a0f4da86deabcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895071"
---
# <a name="importlib-attribute"></a>importlib (attributo)

La **\[ direttiva \] importlib** rende disponibili i tipi già compilati in un'altra libreria dei tipi per la libreria dei tipi in fase di creazione.

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attributi di libreria* 
</dt> <dd>

Zero o più attributi che verranno applicati alla libreria.

</dd> <dt>

*library-name* 
</dt> <dd>

Identificatore che verrà utilizzato da componenti software per indicare questa [**libreria.**](library.md)

</dd> <dt>

*file da importare* 
</dt> <dd>

Nome e percorso del file importato in fase di compilazione MIDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutte **\[ le \] direttive importlib** devono precedere le altre descrizioni dei tipi nella libreria. Si noti che la libreria importata, nonché la libreria generata, devono essere distribuite con l'applicazione in modo che sia disponibile in fase di esecuzione.

Nella maggior parte dei casi è consigliabile usare la direttiva di importazione MIDL **\[** [](import.md) **\]** per fare riferimento alle definizioni da un altro . File IDL nel file . File IDL. Questo metodo fornisce alla libreria dei tipi tutte le informazioni del file originale, mentre **\[ importlib \]** include solo il contenuto della libreria dei tipi.

> [!Note]  
> La **\[ direttiva \] importlib** rende accessibile qualsiasi tipo definito nella libreria importata dall'interno della libreria da compilare. Per evitare ambiguità quando sono presenti riferimenti duplicati, è consigliabile qualificare ogni riferimento con il nome di libreria appropriato, come indicato di seguito:

 

``` syntax
library_name.type
```

In assenza di tale qualifica, MIDL risolve l'ambiguità dei riferimenti duplicati come indicato di seguito:

-   Efficace con la versione 3.1, MIDL usa il primo riferimento trovato.
-   La versione 3.0 di MIDL, la prima versione di MIDL in grado di generare librerie dei tipi, usa l'ultimo riferimento trovato.

## <a name="examples"></a>Esempi

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Libreria**](library.md)
</dt> <dt>

[**Importazione**](import.md)
</dt> <dt>

[Importazione di file di intestazione di sistema](importing-system-header-files.md)
</dt> <dt>

[Importazione di file e librerie dei tipi](importing-files-and-type-libraries.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 