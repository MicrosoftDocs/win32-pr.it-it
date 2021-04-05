---
description: Active Directory fornisce il database degli account utilizzato dall'Centro distribuzione chiavi (KDC) per ottenere informazioni sulle entità di sicurezza nel dominio.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Database account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0713d8f7b4336f43172fcd5cda18aa9d25c702fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967673"
---
# <a name="account-database"></a>Database account

Active Directory fornisce il database degli account utilizzato dall' [*centro distribuzione chiavi*](/windows/desktop/SecGloss/k-gly) (KDC) per ottenere informazioni sulle [*entità di sicurezza*](/windows/desktop/SecGloss/s-gly) nel dominio. Ogni entità è rappresentata da un oggetto account nella directory. La chiave di [*crittografia*](/windows/desktop/SecGloss/e-gly) utilizzata per la comunicazione con un utente, un computer o un servizio viene archiviata come attributo dell'oggetto account di quell'entità di sicurezza.

Solo i controller di dominio sono server Active Directory. Ogni controller di dominio mantiene una copia scrivibile della directory, in modo che sia possibile creare account, reimpostare le password e modificare l'appartenenza a un gruppo in qualsiasi controller di dominio. Le modifiche apportate a una replica della directory vengono automaticamente propagate a tutte le altre repliche. Windows replica l'archivio informazioni per la Active Directory utilizzando un protocollo di replica multimaster proprietario che utilizza una connessione di chiamata a procedura remota sicura tra i partner di replica. La connessione utilizza il [*protocollo di autenticazione Kerberos*](/windows/desktop/SecGloss/k-gly) per fornire [*l'autenticazione*](/windows/desktop/SecGloss/a-gly) e la crittografia reciproche.

L'archiviazione fisica dei dati dell'account viene gestita dall' [agente di sistema di directory](/windows/desktop/AD/directory-system-agent), un processo protetto integrato con l'autorità di [*protezione locale*](/windows/desktop/SecGloss/l-gly) (LSA) nel controller di dominio. Ai client del servizio directory non viene mai concesso l'accesso diretto all'archivio dati. Tutti i client che desiderano accedere alle informazioni della directory devono connettersi all'agente del sistema di directory e quindi cercare, leggere e scrivere oggetti directory e i relativi attributi.

Le richieste di accesso a un oggetto o a un attributo nella directory sono soggette alla convalida da parte dei meccanismi di controllo di accesso di Windows. Analogamente agli oggetti di file e cartelle nel file system NTFS, gli oggetti nel Active Directory sono protetti da [*elenchi di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) che specificano chi può accedere all'oggetto e in che modo. A differenza di file e cartelle, tuttavia, gli oggetti Active Directory hanno un ACL per ognuno dei relativi attributi. Gli attributi per le informazioni riservate sull'account possono pertanto essere protetti da autorizzazioni più restrittive rispetto a quelle concesse per altri attributi dell'account.

Le informazioni più sensibili su un account sono ovviamente la relativa password. Sebbene l'attributo password di un oggetto account archivi una chiave di crittografia derivata da una password, non la password stessa, questa chiave è altrettanto utile per un intruso. Di conseguenza, l'accesso all'attributo password di un oggetto account viene concesso solo al titolare dell'account, mai a chiunque, non ad altri amministratori. Solo i processi con privilegi di base Trusted Computing, ovvero i processi in esecuzione nel [*contesto*](/windows/desktop/SecGloss/c-gly) di sicurezza di LSA, possono leggere o modificare le informazioni sulla password.

Per ostacolare un attacco offline da parte di un utente che ha accesso al nastro di backup di un controller di dominio, l'attributo password di un oggetto account è ulteriormente protetto da una seconda crittografia mediante una chiave di sistema. Questa chiave di crittografia può essere archiviata su supporti rimovibili in modo che sia possibile proteggerla separatamente oppure archiviarla sul controller di dominio, ma protetta da un meccanismo di dispersione. Agli amministratori viene offerta la possibilità di scegliere la posizione in cui viene archiviata la chiave di sistema e quale dei diversi algoritmi viene utilizzata per crittografare gli attributi delle password.

 

 
