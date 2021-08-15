---
title: Classe object e categoria di oggetti
description: Ogni istanza di una classe di oggetti ha una proprietà objectClass multivalore che identifica la classe di cui l'oggetto è un'istanza, nonché tutte le superclassi strutturali o astratte da cui deriva tale classe.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35e7f461caa27e8668cfc47cd94852bf53b291658b828ea017e3dc00a19d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185698"
---
# <a name="object-class-and-object-category"></a>Classe object e categoria di oggetti

Ogni istanza di una classe di oggetti ha una proprietà [**objectClass**](/windows/desktop/ADSchema/a-objectclass) multivalore che identifica la classe di cui l'oggetto è un'istanza, nonché tutte le superclassi strutturali o astratte da cui deriva tale classe. Di conseguenza, la **proprietà objectClass** di un oggetto utente identifica le classi top [**,**](/windows/desktop/ADSchema/c-top) [**person**](/windows/desktop/ADSchema/c-person), [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)e [**user.**](/windows/desktop/ADSchema/c-user) La **proprietà objectClass** non include le classi ausiliarie nell'elenco. Il sistema imposta il **valore objectClass** quando viene creata l'istanza dell'oggetto e non può essere modificato.

Ogni istanza di una classe di oggetti ha anche una proprietà [**objectCategory,**](/windows/desktop/ADSchema/a-objectcategory) ovvero una proprietà a valore singolo che contiene il nome distinto della classe di cui l'oggetto è un'istanza o una delle relative superclassi. Quando viene creato un oggetto, il sistema imposta la proprietà **objectCategory** sul valore specificato dalla proprietà [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) della relativa classe di oggetti. Non è possibile modificare **la proprietà objectCategory** di un oggetto.

Per altre informazioni e un esempio di codice che recupera la proprietà [**objectClass**](/windows/desktop/ADSchema/a-objectclass) di un oggetto, vedere [Recupero dell'attributo objectClass](retrieving-the-objectclass-property.md).

> [!IMPORTANT]
> Prima di Windows Server 2008, [**l'attributo objectClass**](/windows/desktop/ADSchema/a-objectclass) non è indicizzato. Questo perché ha più valori ed è altamente non univoco. in altri, ogni istanza **dell'attributo objectClass** include la [**classe**](/windows/desktop/ADSchema/c-top) principale. Ciò significa che un indice sarebbe molto grande e inefficace. Per individuare gli oggetti di una determinata classe, usare [**l'attributo objectCategory,**](/windows/desktop/ADSchema/a-objectcategory) che è a valore singolo e indicizzato. Per altre informazioni sull'uso di queste proprietà nei filtri di ricerca, vedere [Decidere cosa trovare.](deciding-what-to-find.md)

 

Per la maggior parte delle classi, [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) è il nome distinto dell'oggetto [**classSchema della**](/windows/desktop/ADSchema/c-classschema) classe. Ad esempio, **defaultObjectCategory per** la classe [**organizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit) è "CN=Organizational-Unit,CN=Schema,CN=Configuration,<DC=forestroot>". Tuttavia, alcune classi fanno riferimento a un'altra classe come **defaultObjectCategory**. Ciò consente a una query di trovare facilmente gruppi di oggetti correlati, anche se sono di classi diverse. Ad esempio, le [**classi user**](/windows/desktop/ADSchema/c-user), [**person**](/windows/desktop/ADSchema/c-person), [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)e [**contact**](/windows/desktop/ADSchema/c-contact) identificano tutte la **classe person** nelle proprietà **defaultObjectCategory.** Ciò consente ai filtri di ricerca come (objectCategory=person) di individuare le istanze di tutte queste classi con una singola query. Le query per gli utenti sono molto comuni, quindi si tratta di una semplice ottimizzazione.

Se si crea una sottoclasse da una classe strutturale, è consigliabile impostare il valore [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) della nuova classe sullo stesso nome distinto della superclasse. Ciò consente all'interfaccia utente standard di "trovare" la sottoclasse.

 

 