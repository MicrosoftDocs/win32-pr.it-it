---
description: Le directory nella tabella Directory specificano il layout di un'installazione.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Uso di una proprietà directory in un percorso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa00bf3953be46484d74d3a432135763d1b06d4e7daf72bbc36f284e039613f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141478"
---
# <a name="using-a-directory-property-in-a-path"></a>Uso di una proprietà directory in un percorso

Le directory nella tabella [Directory specificano](directory-table.md) il layout di un'installazione. Quando il Windows installer risolve queste directory durante l'azione [CostFinalize](costfinalize-action.md), le chiavi nella tabella Directory diventano proprietà [impostate](properties.md) sui percorsi di directory. Il programma di installazione imposta sempre anche una serie di Proprietà cartella [di sistema](property-reference.md) standard per i percorsi delle cartelle di sistema.

È garantito che i [valori di Proprietà cartella](property-reference.md) di sistema terminerà con un separatore di directory. I valori di tutte le altre proprietà immesse nella tabella [Directory](directory-table.md) terminano con un separatore di directory solo dopo che il programma di installazione ha eseguito l'azione [CostFinalize](costfinalize-action.md). Prima del completamento della determinazione dei costi, i valori [](property-reference.md) delle proprietà immesse nella tabella Directory che non sono Proprietà cartella di sistema potrebbero non terminare con un separatore di directory. Pertanto, se l'installazione imposta le proprietà della directory usando azioni [personalizzate](custom-actions.md) nel pacchetto, i valori per reference potrebbero non terminare con un separatore di directory.

Le proprietà di directory che terminano con un separatore di directory possono quindi essere usate in una stringa di percorso senza includere in modo esplicito il separatore di directory. Ad esempio, se il valore di DirectoryProperty termina con un separatore di directory, la stringa seguente specifica correttamente il percorso del *file* nella *sottodirectory*

``` syntax
[DirectoryProperty]subdirectory\file
```

e la stringa di percorso seguente non è corretta.

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



