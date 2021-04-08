---
title: Modalità di registrazione dei nomi SPN da un servizio
description: Prima che un client possa utilizzare un nome SPN per autenticare un'istanza di un servizio, è necessario che il nome SPN sia registrato nell'account utente o computer che verrà utilizzato dall'istanza del servizio per l'accesso.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- Modalità di registrazione di un servizio AD SPN
- nome dell'entità servizio AD, come un servizio registra i relativi nomi SPN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74410be3a024fc6accd1d8394e2ba8335be9f550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855426"
---
# <a name="how-a-service-registers-its-spns"></a>Modalità di registrazione dei nomi SPN da un servizio

Prima che un client possa utilizzare un nome SPN per autenticare un'istanza di un servizio, è necessario che il nome SPN sia registrato nell'account utente o computer che verrà utilizzato dall'istanza del servizio per l'accesso. In genere, la registrazione del nome SPN viene eseguita da un programma di installazione del servizio in esecuzione con privilegi di amministratore di dominio.

Il programma di installazione del servizio che installa un'istanza del servizio in un computer host esegue in genere la procedura riportata di seguito.

**Per registrare i nomi SPN per un'istanza del servizio**

1.  Chiamare la funzione [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per creare uno o più nomi SPN univoci per l'istanza del servizio. Per ulteriori informazioni, vedere [formati dei nomi per nomi SPN univoci](name-formats-for-unique-spns.md).
2.  Chiamare la funzione [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) per registrare i nomi nell'account di accesso del servizio.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registra i nomi SPN come proprietà di un oggetto account utente o computer nella directory. gli oggetti **utente** e **computer** hanno un attributo **servicePrincipalName** , che è un attributo multivalore per l'archiviazione di tutti i nomi SPN associati a un account utente o computer. Se il servizio viene eseguito con un account utente, i nomi SPN vengono archiviati nell'attributo **servicePrincipalName** di tale account. Se il servizio viene eseguito nell'account LocalSystem, i nomi SPN vengono archiviati nell'attributo **servicePrincipalName** dell'account del computer host del servizio. Il chiamante **DsWriteAccountSpn** deve specificare il nome distinto dell'oggetto account in cui sono archiviati i nomi SPN.

Per assicurarsi che i nomi SPN registrati siano protetti, l'attributo **servicePrincipalName** non può essere scritto direttamente; può essere scritto solo chiamando [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna). Il chiamante deve disporre dell'accesso in scrittura all'attributo **servicePrincipalName** dell'account di destinazione. Per impostazione predefinita, l'accesso in scrittura viene concesso solo agli amministratori di dominio. Tuttavia, esiste un caso speciale in cui il sistema consente a un servizio in esecuzione con l'account LocalSystem di registrare i propri nomi SPN nell'account computer dell'host del servizio. In questo caso, il nome SPN scritto deve avere il formato " <service class> / <host> " e " &lt; host &gt; " deve corrispondere al nome DNS del computer locale.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) può anche rimuovere i nomi SPN da un account. Un parametro Operation indica se gli SPN devono essere aggiunti all'account, rimossi dall'account o utilizzati per sostituire completamente tutti i nomi SPN correnti per l'account. Quando viene disinstallata un'istanza del servizio, rimuovere tutti i nomi SPN registrati per tale istanza.

Per ulteriori informazioni e un esempio di codice che registra o Annulla la registrazione dei nomi SPN di un servizio, vedere [la pagina relativa alla registrazione dei nomi SPN per un servizio](registering-the-spns-for-a-service.md).

I servizi basati su host che usano il formato SPN semplice " <service class> / <host> " hanno la possibilità di usare la funzione [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) , che consente di creare e registrare i nomi SPN per un'istanza del servizio. **DsServerRegisterSpn** è una funzione di supporto che chiama [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) e [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna).

Per ulteriori informazioni, vedere [account di accesso al servizio](service-logon-accounts.md).

 

 




