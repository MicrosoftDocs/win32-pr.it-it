---
title: Modalità di registrazione dei nomi SPN di un servizio
description: Prima che un client possa utilizzare un nome SPN per autenticare un'istanza di un servizio, è necessario registrare il nome SPN nell'account utente o computer che verrà utilizzato dall'istanza del servizio per l'accesso.
ms.assetid: 39712c1f-3a9a-4c98-a1cb-879ab0b4cb63
ms.tgt_platform: multiple
keywords:
- Come un servizio registra i relativi nomi SPN AD
- nome dell'entità servizio AD , come un servizio registra i relativi nomi SPN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93609ba6205c8075c81204ba5a614a9573d8da5a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881410"
---
# <a name="how-a-service-registers-its-spns"></a>Modalità di registrazione dei nomi SPN di un servizio

Prima che un client possa utilizzare un nome SPN per autenticare un'istanza di un servizio, è necessario registrare il nome SPN nell'account utente o computer che verrà utilizzato dall'istanza del servizio per l'accesso. In genere, la registrazione del nome SPN viene eseguita da un programma di installazione del servizio in esecuzione con privilegi di amministratore di dominio.

Il programma di installazione del servizio che installa un'istanza del servizio in un computer host esegue in genere la procedura seguente.

**Per registrare i nomi SPN per un'istanza del servizio**

1.  Chiamare la [**funzione DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per creare uno o più nomi SPN univoci per l'istanza del servizio. Per altre informazioni, vedere [Formati dei nomi per nomi SPN univoci.](name-formats-for-unique-spns.md)
2.  Chiamare la [**funzione DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) per registrare i nomi nell'account di accesso del servizio.

[**DsWriteAccountSpn registra**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) i nomi SPN come proprietà di un oggetto account utente o computer nella directory. **Gli** oggetti **utente e computer** hanno un attributo **servicePrincipalName,** ovvero un attributo multivalore per l'archiviazione di tutti i nomi SPN associati a un account utente o computer. Se il servizio viene eseguito con un account utente, i nomi SPN vengono archiviati **nell'attributo servicePrincipalName** di tale account. Se il servizio viene eseguito nell'account LocalSystem, i nomi SPN vengono archiviati nell'attributo **servicePrincipalName** dell'account del computer host del servizio. Il **chiamante DsWriteAccountSpn** deve specificare il nome distinto dell'oggetto account in cui sono archiviati i nomi SPN.

Per garantire che i nomi SPN registrati siano sicuri, **l'attributo servicePrincipalName** non può essere scritto direttamente. può essere scritto solo chiamando [**DsWriteAccountSpn.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) Il chiamante deve avere accesso in scrittura **all'attributo servicePrincipalName** dell'account di destinazione. In genere, l'accesso in scrittura viene concesso per impostazione predefinita solo agli amministratori di dominio. Esiste tuttavia un caso speciale in cui il sistema consente a un servizio in esecuzione con l'account LocalSystem di registrare i propri nomi SPN nell'account computer dell'host del servizio. In questo caso, il nome SPN scritto deve avere il formato " host " e " host " deve essere il nome <service class> / &lt; DNS del &gt; computer &lt; &gt; locale.

[**DsWriteAccountSpn può**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) anche rimuovere i nomi SPN da un account. Un parametro dell'operazione indica se i nomi SPN devono essere aggiunti all'account, rimossi dall'account o usati per sostituire completamente tutti i nomi SPN correnti per l'account. Quando un'istanza del servizio viene disinstallata, rimuovere tutti i nomi SPN registrati per tale istanza.

Per altre informazioni e un esempio di codice che registra o annulla la registrazione dei nomi SPN di un servizio, vedere Registrazione dei nomi SPN [per un servizio.](registering-the-spns-for-a-service.md)

I servizi basati su host che usano il formato SPN semplice " host ", hanno la possibilità di usare la funzione <service class> / &lt; &gt; [**DsServerRegisterSpn,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) che crea e registra nomi SPN per un'istanza del servizio. **DsServerRegisterSpn è** una funzione helper che chiama [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) e [**DsWriteAccountSpn.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)

Per altre informazioni, vedere [Account di accesso al servizio.](service-logon-accounts.md)

 

 




