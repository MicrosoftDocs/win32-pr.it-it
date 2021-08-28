---
title: Associazione a Well-Known oggetti con WKGUID
description: Questo argomento illustra come eseguire l'associazione a oggetti usando la stringa di associazione WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Associazione a Well-Known oggetti con WKGUID AD
- Active Directory, uso, associazione, uso di WKGUID per l'associazione a oggetti noti
- oggetti noti AD
- oggetti noti ad Active Directory, associazione a tramite WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d80ab6559a4d4b4d7b620290fd6da7e748a5a5e4e998c0a64c108d99f9e06a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118023689"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a>Associazione a Well-Known oggetti con WKGUID

I contenitori possono avere uno o più sottooggetti importanti che possono essere rinominati o spostati. Può essere difficile tenere traccia di questi sottooggetti e creare stringhe di associazione corrette, soprattutto se vengono rinominati o spostati.

Per supportare l'associazione sicura per la ridenominazione a questi oggetti all'interno di questi contenitori, Active Directory Domain Services due attributi: **wellKnownObjects** e **otherWellKnownObjects**. Questi attributi hanno una sintassi di attributo di ADSTYPE \_ DN \_ WITH \_ BINARY. Consentono più valori e contengono le tuple GUID/DN di oggetti noti all'interno dei contenitori in cui sono impostate. Il server Active Directory mantiene la parte del nome distinto di ogni **voce wellKnownObjects** e **otherWellKnownObjects** in modo che contenga il nome distinto corrente dell'oggetto specificato al momento della creazione della voce.

La **proprietà otherWellKnownObjects** può essere impostata e usata in qualsiasi oggetto.

La **proprietà wellKnownObjects** viene usata nei contenitori domainDNS e configuration. La **proprietà wellKnownObjects** è una proprietà solo di sistema e può essere modificata solo dal sistema operativo.

Il **contenitore domainDNS** include gli oggetti noti seguenti:

-   Utenti
-   Computers (Computer)
-   Sistema
-   Controller di dominio
-   Infrastruttura
-   Oggetti eliminati
-   Persi e trovati

Il contenitore di configurazione ha l'oggetto noto: Oggetti eliminati.

Questi oggetti sono in ogni **dominioDNS** e contenitore di configurazione in un Dominio di Active Directory Service.

È possibile eseguire l'associazione a un oggetto noto usando il formato di associazione WKGUID. L'associazione con WKGUID è supportata solo Active Directory Domain Services, ad esempio il provider LDAP.

> [!IMPORTANT]
> Usare sempre il formato di associazione WKGUID per eseguire l'associazione agli oggetti noti, come elencato in precedenza, nei contenitori di dominio e configurazione. Ciò garantisce che questi contenitori possano essere associati anche se vengono spostati o rinominati.

 

Il formato della stringa di associazione WKGUID è il seguente:


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



" &lt; nome server " è il nome del server di &gt; directory. Il " &lt; nome del server " è &gt; facoltativo.

" XXXXX " è la rappresentazione di stringa del valore esadecimale del &lt; GUID che rappresenta &gt; l'oggetto noto. La stringa GUID viene specificata nel formato "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" e non corrisponde alla stringa GUID prodotta dalla funzione [**StringFromGUID2,**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) che assume il formato "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXXXX}". Per altre informazioni e un esempio di codice che illustra come creare una stringa associabile da un GUID, vedere Codice di esempio per la creazione di una [rappresentazione di](example-code-for-creating-a-bindable-string-representation-of-a-guid.md)stringa associabile di un GUID .

Per eseguire l'associazione a un oggetto specificato in **otherWellKnownObjects** in un oggetto, specificare " XXXXX " come stringa di associazione del GUID noto &lt; &gt; dell'oggetto. Per altre informazioni, vedere [Lettura dell'objectGUID di un](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md)oggetto e Creazione di una rappresentazione di stringa del GUID . Per altre informazioni sull'impostazione della proprietà **otherWellKnownObjects** sugli oggetti, vedere Abilitazione dell'associazione Rename-Safe con la proprietà [otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).

Per eseguire l'associazione a un oggetto specificato in **wellKnownObjects** in domainDNS o contenitori di configurazione, specificare " XXXXX " come una delle costanti seguenti, elencate nella tabella seguente, come definito &lt; &gt; in Ntdsapi.h.



| Contenitore          | Identificatore GUID                         |
|--------------------|-----------------------------------------|
| Utenti              | CONTENITORE \_ UTENTI \_ GUID \_ W               |
| Computers (Computer)          | CONTENITORE \_ GUID COMPUTRS \_ \_ W            |
| Sistema             | CONTENITORE \_ DEI SISTEMI GUID \_ \_ W             |
| Controller di dominio | CONTENITORE \_ CONTROLLER DI DOMINIO GUID \_ \_ \_ W |
| Infrastruttura     | CONTENITORE \_ \_ DELL'INFRASTRUTTURA \_ GUID W      |
| Oggetti eliminati    | CONTENITORE \_ OGGETTI GUID \_ ELIMINATI \_ \_ W    |
| Persi e trovati     | GUID \_ LOSTANDFOUND \_ CONTAINER \_ W        |



 

Ad esempio, per eseguire l'associazione al contenitore utente in un dominio, specificare **GUID \_ USERS CONTAINER \_ \_ W** come " &lt; XXXXX &gt; ".

" DN contenitore " è il nome distinto dell'oggetto contenitore con questo oggetto rappresentato come valore nella relativa proprietà &lt; &gt; **wellKnownObjects.** Ad esempio, per eseguire l'associazione al contenitore users in un dominio, specificare il nome distinto del dominio come " &lt; DN &gt; contenitore ".

Ad esempio, per eseguire l'associazione al contenitore users del dominio Fabrikam.com, usare la stringa di associazione seguente.

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

Per altre informazioni e un esempio di codice che illustra come eseguire l'associazione a un GUID noto, vedere Codice di esempio per l'associazione a [oggetti noti](example-code-for-binding-to-well-known-objects.md).

 

 