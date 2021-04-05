---
title: Problemi di sicurezza per la pubblicazione del servizio
description: Il sistema limita la possibilità di creare, modificare o eliminare oggetti punto di connessione. Quando si pubblica un servizio, è necessario tenere presenti le restrizioni e gestirle.
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- Problemi di sicurezza per Active Directory Service Publication
- Active Directory, utilizzo, sicurezza, problemi di sicurezza della pubblicazione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee5be89c490fa938cdc9c7cf3d7d72434a3dffa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707552"
---
# <a name="security-issues-for-service-publication"></a>Problemi di sicurezza per la pubblicazione del servizio

Il sistema limita la possibilità di creare, modificare o eliminare oggetti punto di connessione. Quando si pubblica un servizio, è necessario tenere presenti le restrizioni e gestirle.

I client devono essere in grado di considerare attendibili i dati pubblicati in un oggetto punto di connessione nella directory. Per questo motivo, l'autorizzazione per la creazione di un oggetto punto di connessione è in genere limitata agli utenti con privilegi, ad esempio gli amministratori di dominio. In questo modo si impedisce agli utenti non autorizzati di ingannare i client creando punti di connessione non validi per i servizi noti.

I servizi non devono essere eseguiti con privilegi di amministratore di dominio. Ciò significa che un servizio non è in genere in grado di creare un punto di connessione. Viene invece fornita un'applicazione di installazione o configurazione del servizio che crea il punto di connessione. Il programma di installazione deve essere eseguito da un utente con i privilegi necessari.

Sebbene un servizio non possa in genere creare il punto di connessione, deve essere in grado di aggiornare le proprietà del punto di connessione in fase di esecuzione. Le proprietà del punto di connessione contengono i dati di associazione utilizzati dai client per la connessione al servizio. Se i dati di binding cambiano, il servizio deve aggiornare il punto di connessione. in caso contrario, i client non potranno utilizzare il servizio. Questo significa che il programma di installazione deve anche modificare il descrittore di sicurezza nell'oggetto punto di connessione per consentire al servizio di leggere e scrivere le proprietà appropriate in fase di esecuzione. Per ulteriori informazioni e un esempio di codice, vedere [Abilitazione dell'account del servizio per l'accesso alle proprietà SCP](enabling-service-account-to-access-scp-properties.md).

Un servizio in esecuzione con l'account LocalSystem può creare un punto di connessione come oggetto figlio sotto il proprio oggetto computer nella directory. Tale servizio rappresenta un'eccezione alla regola dei servizi che non creano punti di connessione. Un servizio LocalSystem dispone inoltre dell'autorizzazione per modificare le proprietà degli oggetti del punto di connessione nel relativo oggetto computer. Tenere presente che un servizio deve essere eseguito con l'account LocalSystem solo se è strettamente necessario. Per ulteriori informazioni, vedere [linee guida per la selezione di un account di accesso al servizio](guidelines-for-selecting-a-service-logon-account.md).

L'applicazione che crea un oggetto punto di connessione o qualsiasi oggetto deve disporre delle autorizzazioni Create Child per la creazione della classe di oggetti nel contenitore in cui verrà creato l'oggetto. Per rimuovere un oggetto, è necessario che il processo che esegue l'operazione disponga delle autorizzazioni Delete Child per la classe Object da eliminare nel contenitore che contiene l'oggetto o che disponga delle autorizzazioni DELETE per l'oggetto stesso. Per aggiornare un punto di connessione, il processo che esegue l'operazione deve disporre dell'accesso in scrittura alle proprietà da aggiornare nell'oggetto.

 

 




