---
description: Le directory della tabella directory specificano il layout di un'installazione.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Utilizzo di una proprietà di directory in un percorso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318975"
---
# <a name="using-a-directory-property-in-a-path"></a>Utilizzo di una proprietà di directory in un percorso

Le directory della [tabella directory](directory-table.md) specificano il layout di un'installazione. Quando il Windows Installer risolve tali directory durante l' [azione CostFinalize secondo](costfinalize-action.md), le chiavi della tabella directory diventano [Proprietà](properties.md) impostate sui percorsi di directory. Il programma di installazione imposta inoltre sempre un numero di [proprietà della cartella di sistema](property-reference.md) standard sui percorsi delle cartelle di sistema.

I valori delle [proprietà della cartella di sistema](property-reference.md) sono sicuramente terminati in un separatore di directory. I valori di tutte le altre proprietà immesse nella [tabella di directory](directory-table.md) possono essere terminati solo in un separatore di directory dopo che il programma di installazione ha eseguito l' [azione CostFinalize secondo](costfinalize-action.md). Prima che i costi siano completati, i valori delle proprietà immesse nella tabella di directory che non sono [proprietà della cartella di sistema](property-reference.md) potrebbero non finire in un separatore di directory. Pertanto, se l'installazione imposta le proprietà della directory utilizzando [azioni personalizzate](custom-actions.md) nel pacchetto, i valori nel riferimento potrebbero non terminare con un separatore di directory.

Le proprietà della directory che terminano con un separatore di directory possono pertanto essere utilizzate in una stringa di percorso senza includere esplicitamente il separatore di directory. Se, ad esempio, il valore di DirectoryProperty termina con un separatore di directory, la stringa seguente specifica correttamente il percorso del *file* nella *sottodirectory*

``` syntax
[DirectoryProperty]subdirectory\file
```

e la stringa di percorso seguente non è corretta.

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



