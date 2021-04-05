---
title: Definizione directory
description: Il componente provider di esempio utilizza una struttura di directory relativamente semplice per chiarire la relazione tra i componenti e per mostrare i requisiti minimi necessari per essere un provider ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855325"
---
# <a name="directory-definition"></a>Definizione directory

Il componente provider di esempio utilizza una struttura di directory relativamente semplice per chiarire la relazione tra i componenti e per mostrare i requisiti minimi necessari per essere un provider ADSI.

"Directory" per il componente provider di esempio è costituito da due nodi radice: "Seattle" e "Toronto". Seattle contiene altri due sottolivelli, "Bellevue" e "Redmond". Ognuna di queste voci contiene diversi account utente. La voce "Toronto" non ha altri sottolivelli, ma contiene direttamente diversi account utente. Nella figura seguente vengono illustrati questi due nodi radice connessi a una rete.

![definizione directory](images/dssmdo.png)

In termini gerarchici, il nodo dello spazio dei nomi contiene "Seattle" e "Toronto". "Seattle" contiene "Bellevue" e "Redmond". "Bellevue" e "Redmond" contengono ognuno un set di account utente. "Toronto" contiene direttamente gli account utente senza nodi organizzativi intermedi.

Il componente provider di esempio rappresenta questa struttura con solo due Active Directory tipi di oggetto: un oggetto contenitore e un oggetto foglia. "Seattle", "Toronto", "Bellevue" e "Redmond" sono oggetti contenitore e ogni account utente è un oggetto foglia.

Il componente provider di esempio crea una classe di schema denominata "unità organizzativa" per un tipo di oggetto contenitore e una classe di schema denominata "User" per un account utente.

Le proprietà per ogni classe dello schema, i relativi metodi e le regole che regolano le relazioni di contenimento per questi oggetti sono tutte definite nella [gestione dello schema](schema-management.md).

 

 




