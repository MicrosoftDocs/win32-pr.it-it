---
title: Classi ausiliarie collegate dinamicamente
description: Una classe ausiliaria collegata in modo dinamico è una classe associata a un singolo oggetto, anziché a una classe di oggetti.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Classi ausiliarie collegate dinamicamente AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5fc73ef64e1ed4af0dd73879dc1cd7ed8b2d82ac1d397db001c1487680b13b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695374"
---
# <a name="dynamically-linked-auxiliary-classes"></a>Classi ausiliarie collegate dinamicamente

Una classe ausiliaria collegata in modo dinamico è una classe associata a un singolo oggetto, anziché a una classe di oggetti. Il collegamento dinamico consente di archiviare attributi aggiuntivi con un singolo oggetto senza l'impatto a livello di foresta dell'estensione della definizione dello schema per un'intera classe. Ad esempio, un'azienda potrebbe usare il collegamento dinamico per collegare una classe ausiliaria specifica delle vendite agli oggetti utente dei suoi venditori e ad altre classi ausiliarie specifiche del reparto agli oggetti utente dei dipendenti di altri reparti.

Il collegamento dinamico non è complesso: aggiungere il nome della classe ausiliaria ai valori dell'attributo **objectClass di un** oggetto. Se la classe ausiliaria ha attributi obbligatori (**mustHave** o **systemMustHave**), è necessario impostarli contemporaneamente. Per altre informazioni e un esempio di codice, vedere [Aggiunta di una classe ausiliaria a un'istanza di oggetto.](adding-an-auxiliary-class-to-an-object-instance.md)

Per rimuovere una classe ausiliaria collegata dinamicamente, cancellare i valori di tutti gli attributi dalla classe ausiliaria e quindi rimuovere il nome della classe ausiliaria dall'attributo **objectClass** dell'oggetto.

Se si aggiunge in modo dinamico una classe ausiliaria che è una sottoclasse di un'altra classe ausiliaria, entrambe le classi ausiliarie vengono aggiunte all'oggetto di destinazione. Tuttavia, la rimozione della classe ausiliaria figlio non ne rimuove l'elemento padre. Ogni classe deve essere rimossa in modo esplicito.

 

 




