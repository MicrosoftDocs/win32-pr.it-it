---
title: Definizione della directory
description: Il componente provider di esempio usa una progettazione di directory relativamente semplice per chiarire la relazione tra i componenti e per mostrare i requisiti minimi necessari per essere un provider ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a46ee47bfa280fb9cffce32480fdad3164a648eee59a0c0b2740834b1f21cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691950"
---
# <a name="directory-definition"></a>Definizione della directory

Il componente provider di esempio usa una progettazione di directory relativamente semplice per chiarire la relazione tra i componenti e per mostrare i requisiti minimi necessari per essere un provider ADSI.

La "directory" per il componente provider di esempio è costituita da due nodi radice: "Seattle" e "Toronto". Seattle contiene altri due sottolivelli, "Bellevue" e "Redmond". Ognuna di queste voci contiene diversi account utente. La voce "Toronto" non ha altri sottolivelli, ma contiene direttamente diversi account utente. La figura seguente mostra questi due nodi radice connessi a una rete.

![definizione di directory](images/dssmdo.png)

In termini gerarchici, il nodo Spazio dei nomi contiene "Seattle" e "Toronto". "Seattle" contiene "Bellevue" e "Redmond". "Bellevue" e "Redmond" contengono ognuno un set di account utente. "Toronto" contiene direttamente gli account utente senza nodi dell'organizzazione intermedi.

Il componente provider di esempio rappresenta questa struttura con solo due tipi di oggetto Active Directory: un oggetto contenitore e un oggetto foglia. "Seattle", "Toronto", "Bellevue" e "Redmond" sono oggetti contenitore e ogni account utente è un oggetto foglia.

Il componente provider di esempio crea una classe di schema denominata "Unità organizzativa" per un tipo di oggetto contenitore e una classe di schema denominata "User" per un account utente.

Le proprietà per ogni classe dello schema, i relativi metodi e le regole che regolano le relazioni di contenimento per questi oggetti sono tutte definite in [Gestione schemi.](schema-management.md)

 

 




