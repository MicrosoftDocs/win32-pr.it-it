---
title: Binding senza server e RootDSE
description: Se possibile, non impostare come hardcoded un nome di server.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Binding senza server e RootDSE AD
- AD binding senza server
- RootDSE AD
- Active Directory, utilizzo, associazione, binding senza server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472483"
---
# <a name="serverless-binding-and-rootdse"></a>Binding senza server e RootDSE

Se possibile, non impostare come hardcoded un nome di server. Inoltre, nella maggior parte dei casi, l'associazione non deve essere necessariamente legata a un singolo server. Active Directory Domain Services supportano il binding senza server, il che significa che Active Directory può essere associato a nel dominio predefinito senza specificare il nome di un controller di dominio. Per le applicazioni ordinarie, si tratta in genere del dominio dell'utente connesso. Per le applicazioni di servizio, si tratta del dominio dell'account di accesso al servizio o del client rappresentato dal servizio.

In LDAP 3,0, rootDSE è definito come la radice dell'albero dei dati di directory in un server di directory. RootDSE non fa parte di alcuno spazio dei nomi. Lo scopo di rootDSE è fornire i dati sul server di directory. Di seguito è riportata la stringa di associazione utilizzata per l'associazione a rootDSE.


```C++
LDAP://<servername>/rootDSE
```



<servername>È il nome DNS di un server. <servername>È facoltativo, come illustrato nel formato seguente.


```C++
LDAP://rootDSE
```



In questo caso, verrà utilizzato un controller di dominio predefinito del dominio in cui si trova il contesto di sicurezza del thread chiamante. Se non è possibile accedere a un controller di dominio all'interno del sito, verrà utilizzato il primo controller di dominio che è possibile individuare.

RootDSE è una posizione nota e affidabile in ogni server di directory per ottenere nomi distinti del dominio, dello schema e dei contenitori di configurazione e di altri dati sul server e il contenuto dell'albero dei dati di directory. Queste proprietà cambiano raramente in un particolare server. Un'applicazione può leggere queste proprietà all'avvio e usarle in tutta la sessione.

In sintesi, un'applicazione deve usare un'associazione senza server per eseguire l'associazione alla directory nel dominio corrente, usare rootDSE per ottenere il nome distinto per uno spazio dei nomi e usare tale nome distinto per l'associazione agli oggetti nello spazio dei nomi.

Per ulteriori informazioni sugli attributi supportati da rootDSE, vedere [RootDSE](/windows/desktop/ADSchema/rootdse) nella documentazione dello Schema di Active Directory.

Per ulteriori informazioni e un esempio di codice che illustra come utilizzare binding senza server e rootDSE, vedere [il codice di esempio per ottenere il nome distinto del dominio](example-code-for-getting-the-distinguished-name-of-the-domain.md).

 

 