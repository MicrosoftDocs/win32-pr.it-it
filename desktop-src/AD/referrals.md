---
title: Riferimenti (AD DS)
description: Active Directory Domain Services mantenere i dati di riferimento negli oggetti crossRef archiviati nel contenitore partizioni (crossRefContainer) nel contenitore di configurazione.
ms.assetid: e4d6cc8a-9c2c-4e0f-acca-e9ecdd5e879b
ms.tgt_platform: multiple
keywords:
- Riferimenti AD
- Active Directory, riferimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63c87fb0248d85ab20191296f9659eb58e460f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299561"
---
# <a name="referrals-ad-ds"></a>Riferimenti (AD DS)

Active Directory Domain Services mantenere i dati di riferimento negli oggetti [**crossRef**](/windows/desktop/ADSchema/c-crossref) archiviati nel contenitore partizioni ([**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer)) nel contenitore di configurazione. Nell'argomento [decidere dove eseguire la ricerca](where-to-search.md) i riferimenti vengono descritti nel contesto di un dominio all'interno di un albero di dominio e la generazione di riferimenti ai domini subordinati in una ricerca di sottoalbero.

Active Directory Domain Services creare e gestire gli oggetti [**crossRef**](/windows/desktop/ADSchema/c-crossref) per tutti i domini della foresta. Sono inoltre disponibili oggetti **crossRef** per i contenitori di configurazione e di schema. Questi oggetti **crossRef** vengono usati per generare riferimenti in risposta a query che richiedono dati sugli oggetti presenti nella foresta, ma non sono contenuti nel server di directory che gestisce la richiesta. Questi sono denominati *riferimenti incrociati interni*, perché fanno riferimento a domini, schemi e contenitori di configurazione all'interno della foresta.

Se la ricerca di riferimenti non è abilitata e viene eseguita una ricerca del sottoalbero, la ricerca restituirà tutti gli oggetti all'interno del dominio specificato che soddisfano i criteri di ricerca. La ricerca restituirà anche i riferimenti a tutti i domini subordinati che sono discendenti diretti del dominio del server di directory. Il client deve risolvere i riferimenti eseguendo l'associazione al percorso specificato dal riferimento e inviando un'altra query.

Se la ricerca dei riferimenti è attivata e viene eseguita una ricerca del sottoalbero, l'API LDAP sottostante tenterà automaticamente di eseguire l'associazione a tutti i riferimenti e di aggiungere i risultati della ricerca al set di risultati. Nella maggior parte dei casi, l'inseguimento dei riferimenti sarà trasparente per il chiamante. Se il riferimento è a un oggetto in un dominio o in una foresta diversa, l'API LDAP sottostante tenterà di usare le credenziali correnti per eseguire il binding alla destinazione del riferimento. Se l'operazione ha esito positivo, l'inseguimento dei riferimenti sarà trasparente. Se l'operazione non riesce, verrà restituito il riferimento e un codice di errore di riferimento.

Per ulteriori informazioni sull'impostazione delle preferenze di ricerca per il rinvio, vedere [specifica di altre opzioni di ricerca](specifying-other-search-options.md).

Oltre alle proprietà [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) (nome DNS del dominio) e [**NCName**](/windows/desktop/ADSchema/a-ncname) (nome distinto per il dominio), l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) contiene anche **NetBiosName** (nome NetBIOS del dominio) e **trustParent** (nome distinto per l'oggetto **crossRef** che rappresenta il dominio padre diretto del dominio).

Active Directory Domain Services possono anche avere *riferimenti incrociati esterni* che fanno riferimento a oggetti all'esterno della foresta. I riferimenti incrociati esterni devono essere aggiunti in modo esplicito da un amministratore. Tenere presente che il server di destinazione del riferimento incrociato esterno deve avere una radice DNS. ovvero deve essere conforme allo standard RFC 2247.

Un riferimento incrociato esterno fa riferimento a un oggetto in qualsiasi altra foresta, purché il nome sia univoco nella foresta di destinazione. Ad esempio, le applicazioni client LDAP utilizzate dall'azienda possono inviare operazioni ai server di directory per Fabrikam.com. Si crea un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) per fabrikam.com. A questo punto, anziché restituire un errore di oggetto non trovato, i server di directory possono restituire un riferimento a un oggetto nel dominio Fabrikam.com e i client possono eseguire il rinvio. Se, ad esempio, si dispone di un oggetto con il nome distinto seguente:


```C++
CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



È possibile aggiungere un riferimento incrociato esterno per un oggetto denominato "ChildOfSomeObject".


```C++
CN=ChildOfSomeObject,CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Una ricerca di sottoalbero che contiene "SomeObject" restituirà anche un riferimento a "ChildOfSomeObject". Tenere presente che deve essere presente un server LDAP all'indirizzo specificato dal riferimento (una delle proprietà nell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) ) e che il server LDAP deve fornire lo spazio dei nomi identificato da "ChildOfSomeObject".

Poiché gli oggetti [**crossRef**](/windows/desktop/ADSchema/c-crossref) vengono archiviati nel contenitore di configurazione, ogni controller di dominio (DC) ha una copia di tutti gli oggetti **crossRef** . Pertanto, ogni controller di dominio contiene dati su ogni dominio della foresta, nonché sulle relazioni superiori/subordinate. Questo consente a ogni controller di dominio di generare riferimenti a qualsiasi dominio nella foresta e i riferimenti per i contenitori di dominio, schema o configurazione subordinati non esplorati in una ricerca di sottoalbero.

Per ulteriori informazioni sui riferimenti, vedere:

-   [Quando vengono generati i riferimenti](when-referrals-are-generated.md)
-   [Creazione di un riferimento esterno](creating-an-external-referral.md)

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come ottenere il nome distinto del contenitore di partizioni, vedere [il codice di esempio per l'individuazione del contenitore di partizioni](example-code-for-locating-the-partitions-container.md).

 

 