---
title: Classe di oggetti e categoria di oggetti
description: Ogni istanza di una classe di oggetti dispone di una proprietà objectClass multivalore che identifica la classe di cui l'oggetto è un'istanza, nonché tutte le superclassi strutturali o astratte da cui viene derivata la classe.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74941b4f32cc197d3dbbf3aa0dc3179b4098ee8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956309"
---
# <a name="object-class-and-object-category"></a>Classe di oggetti e categoria di oggetti

Ogni istanza di una classe di oggetti dispone di una proprietà [**objectClass**](/windows/desktop/ADSchema/a-objectclass) multivalore che identifica la classe di cui l'oggetto è un'istanza, nonché tutte le superclassi strutturali o astratte da cui viene derivata la classe. Quindi, la proprietà **objectClass** di un oggetto utente identificherà le classi [**Top**](/windows/desktop/ADSchema/c-top), [**Person**](/windows/desktop/ADSchema/c-person), [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)e [**User**](/windows/desktop/ADSchema/c-user) . La proprietà **objectClass** non include classi ausiliarie nell'elenco. Il sistema imposta il valore **objectClass** quando viene creata l'istanza dell'oggetto e non può essere modificato.

Ogni istanza di una classe di oggetti dispone anche di una proprietà [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , che è una proprietà a valore singolo che contiene il nome distinto della classe di cui l'oggetto è un'istanza o una delle relative superclassi. Quando viene creato un oggetto, il sistema imposta la relativa proprietà **objectCategory** sul valore specificato dalla proprietà [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) della relativa classe di oggetti. Impossibile modificare la proprietà **objectCategory** di un oggetto.

Per ulteriori informazioni e un esempio di codice che recupera la proprietà [**objectClass**](/windows/desktop/ADSchema/a-objectclass) di un oggetto, vedere [recupero dell'attributo objectClass](retrieving-the-objectclass-property.md).

> [!IMPORTANT]
> Prima di Windows Server 2008, l'attributo [**objectClass**](/windows/desktop/ADSchema/a-objectclass) non è indicizzato. Questo perché contiene più valori ed è altamente non univoco; ovvero ogni istanza dell'attributo **objectClass** include la classe [**Top**](/windows/desktop/ADSchema/c-top) . Ciò significa che un indice sarebbe molto grande e inefficace. Per individuare gli oggetti di una determinata classe, utilizzare l'attributo [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , che è a valore singolo e indicizzato. Per ulteriori informazioni sull'utilizzo di queste proprietà nei filtri di ricerca, vedere la pagina relativa [alla scelta degli elementi da trovare](deciding-what-to-find.md).

 

Per la maggior parte delle classi, [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) è il nome distinto dell'oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) della classe. Ad esempio, il **defaultObjectCategory** per la classe [**ORGANIZATIONALUNIT**](/windows/desktop/ADSchema/c-organizationalunit) è "CN = Organizational-Unit, CN = schema, cn = Configuration, <DC = forestroot>". Alcune classi, tuttavia, fanno riferimento a un'altra classe come **defaultObjectCategory**. Ciò consente a una query di trovare facilmente i gruppi di oggetti correlati, anche se sono di classi diverse. Ad esempio, le classi [**User**](/windows/desktop/ADSchema/c-user), [**Person**](/windows/desktop/ADSchema/c-person), [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)e [**Contact**](/windows/desktop/ADSchema/c-contact) identificano la classe **Person** nelle proprietà **defaultObjectCategory** . Questo consente ai filtri di ricerca come (objectCategory = person) di individuare le istanze di tutte queste classi con una singola query. Le query per gli utenti sono molto comuni, quindi si tratta di una semplice ottimizzazione.

Se si crea una sottoclasse da una classe strutturale, la procedura consigliata consiste nell'impostare il valore [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) della nuova classe sullo stesso nome distinto della superclasse. Ciò consente all'interfaccia utente standard di "trovare" la sottoclasse.

 

 