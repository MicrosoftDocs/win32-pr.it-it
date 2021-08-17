---
description: Active Directory fornisce il database dell'account utilizzato dal Centro distribuzione chiavi (KDC) per ottenere informazioni sulle entità di sicurezza nel dominio.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Database dell'account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4d5e41c959a8c546ef36a5e4014b14ffc949e1670e2b32b199a8c9368bfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141594"
---
# <a name="account-database"></a>Database dell'account

Active Directory fornisce il database dell'account [*utilizzato dal Centro distribuzione chiavi*](/windows/desktop/SecGloss/k-gly) (KDC) per ottenere informazioni sulle entità [*di*](/windows/desktop/SecGloss/s-gly) sicurezza nel dominio. Ogni entità è rappresentata da un oggetto account nella directory . La [*chiave*](/windows/desktop/SecGloss/e-gly) di crittografia utilizzata per comunicare con un utente, un computer o un servizio viene archiviata come attributo dell'oggetto account di tale entità di sicurezza.

Solo i controller di dominio sono server Active Directory. Ogni controller di dominio mantiene una copia scrivibile della directory, in modo che sia possibile creare account, reimpostare le password e modificare l'appartenenza ai gruppi in qualsiasi controller di dominio. Le modifiche apportate a una replica della directory vengono propagate automaticamente a tutte le altre repliche. Windows replica l'archivio informazioni per Active Directory usando un protocollo di replica multiple-master proprietario che usa una connessione remote procedure call protetta tra i partner di replica. La connessione usa il protocollo [*di autenticazione Kerberos per*](/windows/desktop/SecGloss/k-gly) fornire l'autenticazione [*reciproca e*](/windows/desktop/SecGloss/a-gly) la crittografia.

L'archiviazione fisica dei dati dell'account viene gestita dall'agente di sistema [directory,](/windows/desktop/AD/directory-system-agent)un processo protetto integrato con l'autorità di sicurezza locale [](/windows/desktop/SecGloss/l-gly) (LSA) nel controller di dominio. Ai client del servizio directory non viene mai assegnato l'accesso diretto all'archivio dati. Qualsiasi client che desidera accedere alle informazioni della directory deve connettersi all'agente di sistema directory e quindi cercare, leggere e scrivere oggetti directory e i relativi attributi.

Le richieste di accesso a un oggetto o a un attributo nella directory sono soggette alla convalida tramite Windows di controllo di accesso. Analogamente agli oggetti file e cartelle nel file system NTFS, gli [](/windows/desktop/SecGloss/a-gly) oggetti in Active Directory sono protetti da elenchi di controllo di accesso (ACL) che specificano chi può accedere all'oggetto e in che modo. A differenza di file e cartelle, tuttavia, gli oggetti Active Directory hanno un ACL per ognuno dei relativi attributi. Di conseguenza, gli attributi per le informazioni riservate dell'account possono essere protetti da autorizzazioni più restrittive rispetto a quelle concesse per altri attributi dell'account.

Le informazioni più riservate su un account sono ovviamente la relativa password. Anche se l'attributo password di un oggetto account archivia una chiave di crittografia derivata da una password, non la password stessa, questa chiave è utile anche per un intruso. Di conseguenza, l'accesso all'attributo password di un oggetto account viene concesso solo al titolare dell'account, mai a nessun altro utente, nemmeno agli amministratori. Solo i processi con privilegio Trusted Computing [](/windows/desktop/SecGloss/c-gly) Base, ovvero i processi in esecuzione nel contesto di sicurezza dell'LSA, possono leggere o modificare le informazioni sulla password.

Per impedire un attacco offline da parte di un utente con accesso al nastro di backup di un controller di dominio, l'attributo password di un oggetto account è ulteriormente protetto da una seconda crittografia tramite una chiave di sistema. Questa chiave di crittografia può essere archiviata su supporti rimovibili in modo che possa essere protetta separatamente oppure nel controller di dominio ma protetta da un meccanismo di dispersore. Agli amministratori è possibile scegliere dove archiviare la chiave di sistema e quale dei diversi algoritmi viene usato per crittografare gli attributi della password.

 

 
