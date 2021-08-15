---
title: Classi ausiliarie collegate in modo statico
description: Una classe ausiliaria collegata in modo statico è inclusa nell'attributo auxiliaryClass o systemAuxiliaryClass della definizione classSchema di una classe di oggetti nello schema.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Classi ausiliarie collegate in modo statico AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce00592052b1b52f82e2758fdfd7241c6bd24233ce6db6c11389165eeaa5e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024719"
---
# <a name="statically-linked-auxiliary-classes"></a>Classi ausiliarie collegate in modo statico

Una classe ausiliaria collegata in modo statico è inclusa nell'attributo **auxiliaryClass** o **systemAuxiliaryClass** della definizione **classSchema** di una classe di oggetti nello schema. Ciò significa che la classe ausiliaria fa parte di ogni istanza della classe a cui è associata.

Una classe ausiliaria può essere collegata in modo statico a una classe di oggetti quando la classe viene definita, ad esempio quando il relativo **oggetto classSchema** viene aggiunto al contenitore dello schema. Questa è l'unica volta che è possibile usare **systemAuxiliaryClass.** Dopo la creazione di un oggetto **classSchema,** **l'attributo systemAuxiliaryClass** non può essere modificato. Una classe ausiliaria collegata in modo statico in questo momento può avere attributi obbligatori (**mustHave**) e/o facoltativi (**mayHave**).

Un utente con privilegi con le autorizzazioni necessarie per estendere lo schema può aggiungere o rimuovere classi ausiliarie **dall'attributo systemAuxiliaryClass** di un **oggetto classSchema** esistente. In questo modo viene aggiunta o rimossa la classe ausiliaria da ogni istanza esistente della classe di oggetti. Una classe ausiliaria collegata in modo statico in questo momento può avere attributi facoltativi, ma non attributi obbligatori. Ciò è dovuto al fatto che potrebbero essere presenti istanze esistenti della classe di oggetti. In questo caso, l'aggiunta di un nuovo attributo obbligatorio creerebbe problemi. Un utente con privilegi può successivamente rimuovere una classe ausiliaria **dall'attributo auxiliaryClass** di un **oggetto classSchema.**

 

 




