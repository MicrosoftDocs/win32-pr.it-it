---
title: Classi ausiliarie collegate in modo dinamico
description: Una classe ausiliaria collegata dinamicamente è una classe collegata a un singolo oggetto, anziché a una classe di oggetti.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Active Directory classi ausiliarie collegate in modo dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220946"
---
# <a name="dynamically-linked-auxiliary-classes"></a>Classi ausiliarie collegate in modo dinamico

Una classe ausiliaria collegata dinamicamente è una classe collegata a un singolo oggetto, anziché a una classe di oggetti. Il collegamento dinamico consente di archiviare attributi aggiuntivi con un singolo oggetto senza l'effetto a livello di foresta dell'estensione della definizione dello schema per un'intera classe. Ad esempio, un'azienda può utilizzare il collegamento dinamico per collegare una classe ausiliaria specifica alle vendite agli oggetti utente dei propri venditori e altre classi ausiliarie specifiche del reparto agli oggetti utente dei dipendenti in altri reparti.

Il collegamento dinamico non è complesso: aggiungere il nome della classe ausiliaria ai valori dell'attributo **objectClass** di un oggetto. Se la classe ausiliaria ha attributi obbligatori (**musthave** o **systemMustHave**), è necessario impostarli nello stesso momento. Per ulteriori informazioni e un esempio di codice, vedere [aggiunta di una classe ausiliaria a un'istanza dell'oggetto](adding-an-auxiliary-class-to-an-object-instance.md).

Per rimuovere una classe ausiliaria collegata dinamicamente, cancellare i valori di tutti gli attributi dalla classe ausiliaria, quindi rimuovere il nome della classe ausiliaria dall'attributo **objectClass** dell'oggetto.

Se si aggiunge dinamicamente una classe ausiliaria che è una sottoclasse di un'altra classe ausiliaria, entrambe le classi ausiliarie vengono aggiunte all'oggetto di destinazione. Tuttavia, la rimozione della classe ausiliaria figlio non comporta la rimozione dell'elemento padre. ogni classe deve essere rimossa in modo esplicito.

 

 




