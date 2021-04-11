---
title: Abilitazione di Rename-Safe binding con la proprietà otherWellKnownObjects archiviato nel
description: Gli oggetti della classe contenitore hanno un attributo otherWellKnownObjects archiviato nel che è possibile usare per associare un GUID al nome distinto (DN) di un oggetto figlio nel contenitore.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- proprietà otherWellKnownObjects archiviato nel
- proprietà otherWellKnownObjects archiviato nel, utilizzo di per l'associazione Rinomina-Safe
- Active Directory, utilizzo, associazione, associazione Rinomina-Safe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220945"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Abilitazione di Rename-Safe binding con la proprietà otherWellKnownObjects archiviato nel

Gli oggetti della classe contenitore hanno un attributo **otherWellKnownObjects archiviato nel** che è possibile usare per associare un GUID al nome distinto (DN) di un oggetto figlio nel contenitore. Se l'oggetto figlio viene spostato o rinominato, il server di Active Directory aggiorna il DN nel valore **otherWellKnownObjects archiviato nel** per tale oggetto figlio. Questo consente di utilizzare la funzionalità di associazione WKGUID per eseguire l'associazione all'oggetto figlio utilizzando il GUID e il DN del contenitore anziché il DN dell'oggetto figlio.

L'attributo **otherWellKnownObjects archiviato nel** è equivalente all'attributo **wellKnownObjects** ad eccezione del fatto che le applicazioni e i servizi possono scrivere un valore **otherWellKnownObjects archiviato nel** , ma solo il sistema è in grado di scrivere **wellKnownObjects**.

L'uso dell'attributo **otherWellKnownObjects archiviato nel** e dell'associazione WKGUID è vantaggioso nelle situazioni seguenti in cui è necessaria un'associazione Rinomina-safe in relazione a un oggetto contenitore specifico.

Se un oggetto contenitore contiene altri oggetti importanti o se gli oggetti importanti possono essere rinominati o spostati.

Se sono presenti oggetti importanti per ogni istanza dell'oggetto contenitore. Ad esempio, il sistema usa l'attributo **wellKnownObjects** di ogni oggetto **domainDNS** per archiviare un valore per il contenitore Users, presente in ogni istanza di un oggetto **domainDNS** . Questo consente alle applicazioni di eseguire il binding al contenitore degli utenti in modo indipendente dalla ridenominazione specificando il GUID noto e il DN del contenitore **domainDNS** . Le applicazioni possono usare l'attributo **otherWellKnownObjects archiviato nel** di un contenitore in modo analogo.

Se è necessario un binding e/o una funzionalità di ricerca indipendente da rinominare sugli oggetti importanti.

**Per aggiungere le funzionalità di ricerca e associazione Rinomina-Safe**

1.  Aggiungere un valore alla proprietà **otherWellKnownObjects archiviato nel** dell'oggetto contenitore quando viene creato l'oggetto importante in tale contenitore. Il valore contiene il GUID che rappresenta l'oggetto noto. Si noti che questo non è **objectGUID** e **Distinguishname** per l'oggetto.
2.  Utilizzare la funzionalità di associazione WKGUID per eseguire il binding o eseguire ricerche nell'oggetto importante.

L'attributo **otherWellKnownObjects archiviato nel** può avere più valori e contiene le tuple GUID/DN di oggetti noti all'interno dei contenitori in cui sono impostati. L'attributo **otherWellKnownObjects archiviato nel** ha la sintassi DNWithBinary in cui i valori hanno il formato seguente:


```C++
B:<char count>:<well known GUID>:<object DN>
```



In questo esempio, " &lt; char count &gt; " è il numero di cifre esadecimali in " &lt; well known GUID &gt; ", ovvero 32 (numero di cifre esadecimali in un GUID) sia per **otherWellKnownObjects archiviato nel** che per **wellKnownObjects**. " &lt; well known GUID &gt; " è la rappresentazione in cifre esadecimale del GUID noto. " &lt; DN oggetto &gt; " è il nome distinto dell'oggetto rappresentato da questo valore WKO. Il server mantiene la parte ObjectDN di ogni valore **wellKnownObjects** e **otherWellKnownObjects archiviato nel** in modo che contenga il nome distinto corrente dell'oggetto specificato in origine al momento della creazione del valore.

Se, ad esempio, {df447b5e-AA5B-11D2-8D53-00c04f79ab81} è il GUID noto dell'oggetto MyObject nel contenitore di contenuto del dominio Fabrikam.com, il valore di **otherWellKnownObjects archiviato nel** specifica il GUID noto e il DN di oggetto:


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Per eseguire l'associazione a questo oggetto, usare la stringa di associazione WKGUID seguente che specifica il GUID noto dell'oggetto e il DN del contenitore:


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Dopo l'associazione a questo oggetto, è possibile utilizzare le interfacce COM ADSI per cercare, leggere, modificare o eliminare l'oggetto.

Per ulteriori informazioni e un esempio di codice che illustra come aggiungere un oggetto all'attributo **otherWellKnownObjects archiviato nel** , vedere [codice di esempio per la creazione di un oggetto contenitore](example-code-for-creating-a-container-object.md).

 

 




