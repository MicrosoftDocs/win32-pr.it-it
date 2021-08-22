---
title: Abilitazione Rename-Safe binding con la proprietà otherWellKnownObjects
description: Gli oggetti della classe Container hanno un attributo otherWellKnownObjects che è possibile usare per associare un GUID al nome distinto (DN) di un oggetto figlio nel contenitore.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- otherWellKnownObjects - proprietà
- proprietà otherWellKnownObjects, uso di per l'associazione indipendente dalla ridenominazione
- Active Directory, uso, associazione, associazione indipendente dalla ridenominazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446f669adc9a59f9f8aba93e852546fe3991952857469d6f37978d9cf91a7666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695320"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Abilitazione Rename-Safe binding con la proprietà otherWellKnownObjects

Gli oggetti della classe Container hanno un attributo **otherWellKnownObjects** che è possibile usare per associare un GUID al nome distinto (DN) di un oggetto figlio nel contenitore. Se l'oggetto figlio viene spostato o rinominato, il server Active Directory aggiorna il DN nel valore **otherWellKnownObjects** per tale oggetto figlio. In questo modo è possibile usare la funzionalità di associazione WKGUID per eseguire l'associazione all'oggetto figlio usando il GUID e il DN del contenitore anziché il DN dell'oggetto figlio.

**L'attributo otherWellKnownObjects** è equivalente all'attributo **wellKnownObjects,** ad eccezione del fatto che applicazioni e servizi possono scrivere un valore **otherWellKnownObjects,** ma solo il sistema può scrivere **wellKnownObjects**.

**L'uso dell'attributo otherWellKnownObjects** e dell'associazione WKGUID è utile nelle situazioni seguenti in cui è necessaria l'associazione indipendente dalla ridenominazione in relazione a un oggetto contenitore specifico.

Se un oggetto contenitore contiene altri oggetti importanti o se gli oggetti importanti possono essere rinominati o spostati.

Se esistono oggetti importanti per ogni istanza dell'oggetto contenitore. Ad esempio, il sistema usa l'attributo **wellKnownObjects** di ogni oggetto **domainDNS** per archiviare un valore per il contenitore Users, presente in ogni istanza di un **oggetto domainDNS.** In questo modo le applicazioni possono eseguire l'associazione al contenitore Users in modo sicuro specificando il GUID noto e il DN del **contenitore domainDNS.** Le applicazioni possono usare in modo analogo **l'attributo otherWellKnownObjects** di un contenitore.

Se è necessaria l'associazione e/o la funzionalità di ricerca indipendente dalla ridenominazione per gli oggetti importanti.

**Per aggiungere funzionalità di associazione e ricerca sicure per la ridenominazione**

1.  Aggiungere un valore alla proprietà **otherWellKnownObjects** dell'oggetto contenitore quando l'oggetto importante viene creato all'interno di tale contenitore. Il valore contiene il GUID che rappresenta l'oggetto noto. Tenere presente che non si tratta di **objectGUID** e **distinguishedName** per tale oggetto.
2.  Usare la funzionalità di associazione WKGUID per eseguire l'associazione o la ricerca nell'oggetto importante.

**L'attributo otherWellKnownObjects** può avere più valori e contiene le tuple GUID/DN di oggetti noti all'interno dei contenitori in cui sono impostate. **L'attributo otherWellKnownObjects** ha la sintassi DNWithBinary in cui i valori hanno il formato seguente:


```C++
B:<char count>:<well known GUID>:<object DN>
```



In questo esempio " char count " è il conteggio delle cifre esadecimali in " WELL KNOWN GUID ", ovvero 32 (numero di cifre &lt; &gt; &lt; &gt; esadecimali in un GUID) per **otherWellKnownObjects** e **wellKnownObjects**. " &lt; GUID noto " è la &gt; rappresentazione in cifre esadecimali del GUID noto. " &lt; object DN &gt; " è il nome distinto dell'oggetto rappresentato da questo valore WKO. Il server mantiene la parte ObjectDN di ogni **valore wellKnownObjects** e **otherWellKnownObjects** in modo che contenga il nome distinto corrente dell'oggetto specificato in origine al momento della creazione del valore.

Ad esempio, se {df447b5e-aa5b-11d2-8d53-00c04f79ab81} è il GUID noto dell'oggetto MyObject nel contenitore MyContainer nel dominio Fabrikam.com, il valore **otherWellKnownObjects** specifica il GUID noto e il DN di MyObject:


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Per eseguire l'associazione a questo oggetto, usare la stringa di associazione WKGUID seguente che specifica il GUID noto dell'oggetto e il DN del contenitore:


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Dopo l'associazione a questo oggetto, è possibile usare le interfacce COM ADSI per cercare, leggere, modificare o eliminare l'oggetto.

Per altre informazioni e un esempio di codice che illustra come aggiungere un oggetto **all'attributo otherWellKnownObjects,** vedere Codice di esempio per la creazione di [un oggetto contenitore.](example-code-for-creating-a-container-object.md)

 

 




