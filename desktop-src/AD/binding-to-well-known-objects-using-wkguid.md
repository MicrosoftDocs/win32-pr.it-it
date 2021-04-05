---
title: Associazione a oggetti Well-Known mediante WKGUID
description: In questo argomento viene illustrato come eseguire l'associazione a oggetti utilizzando la stringa di associazione WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Associazione a oggetti Well-Known con WKGUID AD
- Active Directory, utilizzo di, associazione, utilizzo di WKGUID per l'associazione a oggetti noti
- oggetti noti AD
- oggetti noti AD, associazione all'uso di WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724647"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a>Associazione a oggetti Well-Known mediante WKGUID

I contenitori possono avere uno o più oggetti importanti che possono essere rinominati o spostati. Può essere difficile tenere traccia di questi oggetti e compilare stringhe di binding corrette, soprattutto se vengono rinominati o spostati.

Per supportare l'associazione Rinomina-safe a questi oggetti all'interno di questi contenitori, Active Directory Domain Services hanno due attributi: **wellKnownObjects** e **otherWellKnownObjects archiviato nel**. Questi attributi hanno una sintassi di attributo ADSTYPE \_ DN \_ con \_ Binary. Consentono più valori e contengono tuple GUID/DN di oggetti noti all'interno dei contenitori sui quali sono impostati. Il server Active Directory gestisce la parte del nome distinto di ogni voce **wellKnownObjects** e **otherWellKnownObjects archiviato nel** in modo che contenga il nome distinto corrente dell'oggetto specificato al momento della creazione della voce.

È possibile impostare e usare la proprietà **otherWellKnownObjects archiviato nel** in qualsiasi oggetto.

La proprietà **wellKnownObjects** viene usata nei contenitori domainDNS e Configuration. La proprietà **wellKnownObjects** è una proprietà solo di sistema e può essere modificata solo dal sistema operativo.

Il contenitore **domainDNS** dispone dei seguenti oggetti noti:

-   Utenti
-   Computers (Computer)
-   Sistema
-   Controller di dominio
-   Infrastruttura
-   Oggetti eliminati
-   Perso e trovato

Il contenitore di configurazione dispone degli oggetti noti: Deleted Objects.

Questi oggetti si trovano in ogni contenitore di **domainDNS** e configurazione in un servizio dominio di Active Directory.

È possibile eseguire il binding a un oggetto noto usando il formato di associazione WKGUID. Il binding con WKGUID è supportato solo in Active Directory Domain Services, ovvero il provider LDAP.

> [!IMPORTANT]
> Usare sempre il formato di associazione WKGUID per eseguire l'associazione agli oggetti noti, come elencato in precedenza, nei contenitori di dominio e configurazione. In questo modo si garantisce che questi contenitori possano essere associati a anche se vengono spostati o rinominati.

 

Il formato della stringa di binding WKGUID è il seguente:


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



" &lt; nome server &gt; " è il nome del server di directory. Il &lt; nome del server &gt; è facoltativo.

" &lt; Xxxxx &gt; " è la rappresentazione di stringa del valore esadecimale del GUID che rappresenta l'oggetto noto. La stringa GUID viene specificata nel form "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" e non ha lo stesso formato della stringa GUID prodotta dalla funzione [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , che assume il formato "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}". Per ulteriori informazioni e un esempio di codice in cui viene illustrato come creare una stringa associabile da un GUID, vedere [codice di esempio per la creazione di una rappresentazione di stringa associabile di un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).

Per eseguire l'associazione a un oggetto specificato in **otherWellKnownObjects archiviato nel** in un oggetto, specificare " &lt; xxxxx &gt; " come formato stringa di binding del GUID dell'oggetto noto dell'oggetto. Per altre informazioni, vedere [lettura di objectGUID di un oggetto e creazione di una rappresentazione di stringa del GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md). Per ulteriori informazioni sull'impostazione della proprietà **otherWellKnownObjects archiviato nel** sugli oggetti, vedere [Abilitazione dell'associazione Rename-Safe con la proprietà otherWellKnownObjects archiviato nel](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).

Per eseguire l'associazione a un oggetto specificato in **wellKnownObjects** in domainDNS o nei contenitori di configurazione, specificare " &lt; xxxxx &gt; " come una delle seguenti costanti, elencate nella tabella seguente, come definito in ntdsapi. h.



| Contenitore          | Identificatore GUID                         |
|--------------------|-----------------------------------------|
| Utenti              | \_contenitore utenti \_ GUID \_ W               |
| Computers (Computer)          | \_contenitore di calcolo \_ GUID \_ W            |
| Sistema             | \_contenitore di sistemi GUID \_ \_ W             |
| Controller di dominio | \_contenitore controller di dominio GUID \_ \_ \_ W |
| Infrastruttura     | \_contenitore infrastruttura \_ GUID \_ W      |
| Oggetti eliminati    | \_ \_ contenitore oggetti eliminati \_ GUID \_ W    |
| Perso e trovato     | GUID \_ LOSTANDFOUND \_ contenitore \_ W        |



 

Ad esempio, per eseguire l'associazione al contenitore utente in un dominio, specificare **GUID \_ Users \_ Container \_ W** come " &lt; xxxxx &gt; ".

" &lt; contenitore DN &gt; " è il nome distinto dell'oggetto contenitore con questo oggetto rappresentato come valore nella relativa proprietà **wellKnownObjects** . Ad esempio, per eseguire l'associazione al contenitore degli utenti in un dominio, specificare il nome distinto del dominio come " &lt; DN del contenitore &gt; ".

Ad esempio, per eseguire l'associazione al contenitore Users del dominio Fabrikam.com, usare la stringa di binding seguente.

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire l'associazione a un GUID noto, vedere il [codice di esempio per l'associazione a oggetti noti](example-code-for-binding-to-well-known-objects.md).

 

 