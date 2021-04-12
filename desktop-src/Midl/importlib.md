---
title: importlib (attributo)
description: La direttiva \ importlib \ rende disponibili i tipi già compilati in un'altra libreria dei tipi per la libreria dei tipi in fase di creazione.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- attributo MIDL di importlib
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472766"
---
# <a name="importlib-attribute"></a>importlib (attributo)

La direttiva **\[ importlib \]** rende disponibili i tipi che sono già stati compilati in un'altra libreria dei tipi per la libreria dei tipi creata.

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

*Library-attributi* 
</dt> <dd>

Zero o più attributi che verranno applicati alla libreria.

</dd> <dt>

*nome della libreria* 
</dt> <dd>

Identificatore che i componenti software utilizzeranno per indicare la [**libreria**](library.md).

</dd> <dt>

*da file a importazione* 
</dt> <dd>

Nome e percorso del file importato in fase di compilazione MIDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutte le direttive **\[ importlib \]** devono precedere le altre descrizioni dei tipi nella libreria. Si noti che la libreria importata, così come la libreria generata, deve essere distribuita con l'applicazione in modo che sia disponibile in fase di esecuzione.

Nella maggior parte dei casi è consigliabile usare la **\[** [](import.md) **\]** direttiva di importazione MIDL per fare riferimento alle definizioni di un altro. File IDL nel. File IDL. Questo metodo fornisce alla libreria dei tipi tutte le informazioni del file originale, mentre **\[ importlib \]** porta solo il contenuto della libreria dei tipi.

> [!Note]  
> La direttiva **\[ importlib \]** rende accessibili tutti i tipi definiti nella libreria importata dalla libreria in fase di compilazione. Per evitare ambiguità in presenza di riferimenti duplicati, è consigliabile qualificare ogni riferimento con il nome della libreria appropriato, come indicato di seguito:

 

``` syntax
library_name.type
```

In assenza di tale qualificazione, MIDL risolve ambiguità di riferimento duplicata come indicato di seguito:

-   A partire dalla versione 3,1, MIDL usa il primo riferimento rilevato.
-   La versione 3,0 di MIDL, la prima versione di MIDL che può generare librerie dei tipi, usa l'ultimo riferimento rilevato.

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

[**libreria**](library.md)
</dt> <dt>

[**importare**](import.md)
</dt> <dt>

[Importazione di file di intestazione di sistema](importing-system-header-files.md)
</dt> <dt>

[Importazione di file e librerie dei tipi](importing-files-and-type-libraries.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 