---
title: Utilizzo di objectGUID per l'associazione a un oggetto
description: Il nome distinto di un oggetto viene modificato se l'oggetto viene rinominato o spostato, pertanto il nome distinto non è un identificatore di oggetto affidabile.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Utilizzo di objectGUID per l'associazione a un oggetto AD
- objectGUID AD
- objectGUID AD, utilizzo di per l'associazione a un oggetto
- Active Directory, utilizzo di, associazione, utilizzo di objectGUID per l'associazione all'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046477"
---
# <a name="using-objectguid-to-bind-to-an-object"></a>Utilizzo di objectGUID per l'associazione a un oggetto

Il nome distinto di un oggetto viene modificato se l'oggetto viene rinominato o spostato, pertanto il nome distinto non è un identificatore di oggetto affidabile. In Active Directory Domain Services la proprietà **objectGUID** di un oggetto non cambia mai, anche se l'oggetto è stato rinominato o spostato. Per ulteriori informazioni su **objectGUID** e sugli identificatori, vedere [nomi e identità degli oggetti](object-names-and-identities.md).

Il provider LDAP Active Directory fornisce un metodo per l'associazione a un oggetto mediante il GUID dell'oggetto. Il formato della stringa di binding è il seguente:


```C++
LDAP://servername/<GUID=XXXXX>
```



In questo esempio "ServerName" è il nome del server di directory e "XXXXX" è la rappresentazione di stringa del valore esadecimale del GUID. "ServerName" è facoltativo. La stringa GUID viene specificata nel form "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX". La stringa GUID può inoltre assumere il formato "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", che è lo stesso formato della stringa prodotta dalla funzione [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , senza le parentesi graffe circostanti " {} ". Per ulteriori informazioni e un esempio di codice in cui viene illustrato come creare una stringa associabile da un GUID, vedere [codice di esempio per la creazione di una rappresentazione di stringa associabile di un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md). È possibile utilizzare la proprietà [**IADs. Guid**](/windows/desktop/ADSI/iads-property-methods) per recuperare il formato stringa corretto del GUID.

Quando si esegue l'associazione con il GUID dell'oggetto, alcuni metodi e proprietà [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) non sono supportati. Le proprietà **IADs** seguenti non sono supportate dagli oggetti ottenuti tramite binding mediante il GUID dell'oggetto:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nome**](/windows/desktop/ADSI/iads-property-methods)
-   [**Padre**](/windows/desktop/ADSI/iads-property-methods)

I metodi **IADsContainer** seguenti non sono supportati dagli oggetti ottenuti dall'associazione usando il GUID dell'oggetto:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Creare**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Per utilizzare questi metodi e proprietà dopo l'associazione a un oggetto utilizzando il GUID dell'oggetto, utilizzare il metodo [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare il nome distinto dell'oggetto e quindi utilizzare il nome distinto per associare nuovamente l'oggetto.

Se un'applicazione archivia o memorizza nella cache gli identificatori o i riferimenti agli oggetti archiviati in Active Directory Domain Services, il GUID dell'oggetto è l'identificatore migliore da usare per diversi motivi:

-   La proprietà **objectGUID** di sull'oggetto non cambia mai anche se l'oggetto è stato rinominato o spostato.
-   È facile eseguire l'associazione all'oggetto usando il GUID dell'oggetto.
-   Se l'oggetto viene rinominato o spostato, la proprietà **objectGUID** fornisce un identificatore singolo che può essere usato per trovare e identificare rapidamente l'oggetto anziché dover comporre una query con condizioni per tutte le proprietà che identificano tale oggetto.

 

 