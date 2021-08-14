---
title: Modalità di registrazione dei nomi SPN da parte di un servizio
description: Prima che un client possa usare un nome SPN per autenticare un'istanza di un servizio, il nome SPN deve essere registrato nell'account utente o computer che verrà utilizzato dall'istanza del servizio per accedere.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- Modalità di registrazione dei nomi SPN da parte di un servizio
- nome dell'entità servizio AD , come un servizio registra i nomi SPN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ebf33ed0f28dff3acffdcdc96a880c21ec532ff677801dd52ac1801f44c80e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188584"
---
# <a name="how-a-service-registers-its-spns"></a>Modalità di registrazione dei nomi SPN da parte di un servizio

Prima che un client possa usare un nome SPN per autenticare un'istanza di un servizio, il nome SPN deve essere registrato nell'account utente o computer che verrà utilizzato dall'istanza del servizio per accedere. In genere, la registrazione del nome SPN viene eseguita da un programma di installazione del servizio in esecuzione con privilegi di amministratore di dominio.

Il programma di installazione del servizio che installa un'istanza del servizio in un computer host esegue in genere la procedura seguente.

**Per registrare nomi SPN per un'istanza del servizio**

1.  Chiamare la [**funzione DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per creare uno o più nomi SPN univoci per l'istanza del servizio. Per altre informazioni, vedere [Formati dei nomi per nomi SPN univoci](name-formats-for-unique-spns.md).
2.  Chiamare la [**funzione DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) per registrare i nomi nell'account di accesso del servizio.

[**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registra i nomi SPN come proprietà di un oggetto account utente o computer nella directory. **Gli** oggetti **utente e computer** hanno un attributo **servicePrincipalName,** ovvero un attributo multivalore per l'archiviazione di tutti i nomi SPN associati a un account utente o computer. Se il servizio viene eseguito con un account utente, i nomi SPN vengono archiviati **nell'attributo servicePrincipalName** di tale account. Se il servizio viene eseguito nell'account LocalSystem, i nomi SPN vengono archiviati **nell'attributo servicePrincipalName** dell'account del computer host del servizio. Il **chiamante DsWriteAccountSpn** deve specificare il nome distinto dell'oggetto account in cui vengono archiviati i nomi SPN.

Per garantire che i nomi SPN registrati siano sicuri, **l'attributo servicePrincipalName** non può essere scritto direttamente. può essere scritto solo chiamando [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna). Il chiamante deve avere accesso in scrittura **all'attributo servicePrincipalName** dell'account di destinazione. In genere, l'accesso in scrittura viene concesso per impostazione predefinita solo agli amministratori di dominio. Esiste tuttavia un caso speciale in cui il sistema consente a un servizio in esecuzione con l'account LocalSystem di registrare i propri nomi SPN nell'account computer dell'host del servizio. In questo caso, il nome SPN scritto deve avere il formato " " e " host " deve essere il nome <service class> / <host> DNS del &lt; computer &gt; locale.

[**DsWriteAccountSpn può**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) anche rimuovere nomi SPN da un account. Un parametro dell'operazione indica se i nomi SPN devono essere aggiunti all'account, rimossi dall'account o usati per sostituire completamente tutti i nomi SPN correnti per l'account. Quando un'istanza del servizio viene disinstallata, rimuovere tutti i nomi SPN registrati per tale istanza.

Per altre informazioni e un esempio di codice che registra o annulla la registrazione dei nomi SPN di un servizio, vedere Registrazione dei nomi [SPN per un servizio](registering-the-spns-for-a-service.md).

I servizi basati su host che usano il formato SPN semplice " ", hanno la possibilità di usare la funzione <service class> / <host> [**DsServerRegisterSpn,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) che crea e registra nomi SPN per un'istanza del servizio. **DsServerRegisterSpn è** una funzione helper che chiama [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) e [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna).

Per altre informazioni, vedere [Account di accesso al servizio](service-logon-accounts.md).

 

 




