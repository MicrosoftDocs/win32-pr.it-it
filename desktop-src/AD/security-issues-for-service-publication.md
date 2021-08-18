---
title: Problemi di sicurezza per la pubblicazione del servizio
description: Il sistema limita la possibilità di creare, modificare o eliminare oggetti punto di connessione. Tenere presenti e gestire queste restrizioni quando si pubblica un servizio.
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- Problemi di sicurezza per la pubblicazione del servizio AD
- Active Directory, uso, sicurezza, problemi di sicurezza della pubblicazione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e4cec29d08a029bca52a99b573eb339964dd42274d3ca2e54795bb80b60897
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024909"
---
# <a name="security-issues-for-service-publication"></a>Problemi di sicurezza per la pubblicazione del servizio

Il sistema limita la possibilità di creare, modificare o eliminare oggetti punto di connessione. Tenere presenti e gestire queste restrizioni quando si pubblica un servizio.

I client devono essere in grado di considerare attendibili i dati pubblicati in un oggetto punto di connessione nella directory. Per questo motivo, l'autorizzazione per creare un oggetto punto di connessione è in genere limitata agli utenti con privilegi, ad esempio gli amministratori di dominio. Ciò impedisce agli utenti non autorizzati di ingannare i client creando punti di connessione non validi per i servizi noti.

I servizi non devono essere eseguiti con privilegi di amministratore di dominio. Ciò significa che un servizio in genere non può creare un proprio punto di connessione. Si fornisce invece un'applicazione di configurazione o di installazione del servizio che crea il punto di connessione. Questo programma di installazione deve essere eseguito da un utente con i privilegi necessari.

Anche se un servizio in genere non può creare il proprio punto di connessione, deve essere in grado di aggiornare le proprietà del punto di connessione in fase di esecuzione. Le proprietà del punto di connessione contengono i dati di associazione usati dai client per connettersi al servizio. Se i dati di associazione cambiano, il servizio deve aggiornare il punto di connessione. In caso contrario, i client non possono usare il servizio. Ciò significa che il programma di installazione deve anche modificare il descrittore di sicurezza nell'oggetto punto di connessione per consentire al servizio di leggere e scrivere le proprietà appropriate in fase di esecuzione. Per altre informazioni e un esempio di codice, vedere [Abilitazione dell'account del servizio per l'accesso alle proprietà SCP](enabling-service-account-to-access-scp-properties.md).

Un servizio in esecuzione con l'account LocalSystem può creare un punto di connessione come oggetto figlio sotto il proprio oggetto computer nella directory. Tale servizio è un'eccezione alla regola dei servizi che non creano i propri punti di connessione. Un servizio LocalSystem dispone anche dell'autorizzazione per modificare le proprietà degli oggetti punto di connessione nel proprio oggetto computer. Tenere presente che un servizio deve essere eseguito con l'account LocalSystem solo se assolutamente necessario. Per altre informazioni, vedere [Linee guida per la selezione di un account di accesso al servizio.](guidelines-for-selecting-a-service-logon-account.md)

L'applicazione che crea un oggetto punto di connessione o qualsiasi oggetto deve disporre delle autorizzazioni figlio per la classe di oggetti da creare nel contenitore in cui verrà creato l'oggetto. Per rimuovere un oggetto, il processo che esegue l'operazione deve disporre delle autorizzazioni di eliminazione figlio per la classe di oggetto da eliminare nel contenitore che contiene l'oggetto o avere autorizzazioni di eliminazione per l'oggetto stesso. Per aggiornare un punto di connessione, il processo che esegue l'operazione deve avere accesso in scrittura alle proprietà da aggiornare nell'oggetto .

 

 




