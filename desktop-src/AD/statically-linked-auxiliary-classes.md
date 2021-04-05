---
title: Classi ausiliarie collegate in modo statico
description: Una classe ausiliaria collegata in modo statico è una classe inclusa nell'attributo auxiliaryClass o systemAuxiliaryClass della definizione classSchema di una classe di oggetti nello schema.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Active Directory (classi ausiliarie) collegate in modo statico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707537"
---
# <a name="statically-linked-auxiliary-classes"></a>Classi ausiliarie collegate in modo statico

Una classe ausiliaria collegata in modo statico è una classe inclusa nell'attributo **auxiliaryClass** o **SystemAuxiliaryClass** della definizione **classSchema** di una classe di oggetti nello schema. Ciò significa che la classe ausiliaria fa parte di ogni istanza della classe a cui è associata.

Una classe ausiliaria può essere collegata in modo statico a una classe di oggetti quando la classe è definita, ovvero quando il relativo oggetto **classSchema** viene aggiunto al contenitore dello schema. Questa è l'unica volta in cui è possibile usare **systemAuxiliaryClass** . Dopo la creazione di un oggetto **classSchema** , non è possibile modificare l'attributo **systemAuxiliaryClass** . Una classe ausiliaria collegata in modo statico in questo momento può avere attributi obbligatori (**musthave**) e/o facoltativi (**Faran**).

Un utente con privilegi con le autorizzazioni necessarie per estendere lo schema può aggiungere o rimuovere classi ausiliarie dall'attributo **systemAuxiliaryClass** di un oggetto **classSchema** esistente. In questo modo viene aggiunta o rimossa la classe ausiliaria da tutte le istanze esistenti della classe di oggetti. Una classe ausiliaria collegata in modo statico in questo momento può avere attributi facoltativi, ma non può avere attributi obbligatori. Ciò è dovuto al fatto che possono esistere istanze della classe di oggetti. in questo caso, l'aggiunta di un nuovo attributo obbligatorio comporta la creazione di problemi. Un utente con privilegi può quindi rimuovere una classe ausiliaria dall'attributo **auxiliaryClass** di un oggetto **classSchema** .

 

 




