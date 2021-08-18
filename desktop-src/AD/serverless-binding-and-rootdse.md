---
title: Associazione serverless e RootDSE
description: Se possibile, non codificare a livello di codice un nome di server.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Associazione serverless e RootDSE AD
- Ad associazione serverless
- RootDSE AD
- Active Directory, uso, associazione, associazione serverless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3c88386ae95efdebd031199e135ff4c5d610e402b9cba522256df5eef097e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024929"
---
# <a name="serverless-binding-and-rootdse"></a>Associazione serverless e RootDSE

Se possibile, non codificare a livello di codice un nome di server. Inoltre, nella maggior parte dei casi, l'associazione non deve essere inutilmente associata a un singolo server. Active Directory Domain Services supportano l'associazione serverless, il che significa che Active Directory può essere associato a nel dominio predefinito senza specificare il nome di un controller di dominio. Per le applicazioni normali, questo è in genere il dominio dell'utente connesso. Per le applicazioni di servizio, si tratta del dominio dell'account di accesso al servizio o del client rappresentato dal servizio.

In LDAP 3.0 rootDSE è definito come radice dell'albero dei dati della directory in un server di directory. RootDSE non fa parte di alcuno spazio dei nomi. Lo scopo di rootDSE è fornire dati sul server di directory. Di seguito è riportata la stringa di associazione utilizzata per l'associazione a rootDSE.


```C++
LDAP://<servername>/rootDSE
```



è <servername> il nome DNS di un server. è <servername> facoltativo, come illustrato nel formato seguente.


```C++
LDAP://rootDSE
```



In questo caso, verrà usato un controller di dominio predefinito del dominio in cui si trova il contesto di sicurezza del thread chiamante. Se non è possibile accedere a un controller di dominio all'interno del sito, verrà utilizzato il primo controller di dominio trovato.

RootDSE è un percorso noto e affidabile in ogni server di directory per ottenere nomi distinti dei contenitori di dominio, schema e configurazione e altri dati relativi al server e al contenuto dell'albero dei dati della directory. Queste proprietà cambiano raramente in un determinato server. Un'applicazione può leggere queste proprietà all'avvio e usarle per tutta la sessione.

In breve, un'applicazione deve usare l'associazione serverless per eseguire l'associazione alla directory nel dominio corrente, usare rootDSE per ottenere il nome distinto per uno spazio dei nomi e usare tale nome distinto per l'associazione agli oggetti nello spazio dei nomi.

Per altre informazioni sugli attributi supportati da rootDSE, vedere [RootDSE](/windows/desktop/ADSchema/rootdse) nella documentazione relativa allo schema di Active Directory.

Per altre informazioni e un esempio di codice che illustra come usare l'associazione serverless e rootDSE, vedere Codice di esempio per ottenere il nome distinto [del dominio](example-code-for-getting-the-distinguished-name-of-the-domain.md).

 

 