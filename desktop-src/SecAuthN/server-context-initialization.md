---
description: Come il client, il server acquisisce anche un handle di credenziali per essere pronto a rispondere a una richiesta di autenticazione in ingresso dal client.
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: Inizializzazione del contesto server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1362c8fd71e079392f10a8e35f76ad511de3c49f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756416"
---
# <a name="server-context-initialization"></a>Inizializzazione del contesto server

Come il client, il server acquisisce anche un handle di [*credenziali*](../secgloss/c-gly.md) per essere pronto a rispondere a una richiesta di autenticazione in ingresso dal client. Le credenziali del server vengono utilizzate per autenticare il server nel client in [*protocolli di sicurezza*](../secgloss/s-gly.md) che supportano l'autenticazione server o l'autenticazione reciproca. Il server ottiene un handle per le credenziali definite dall'account del servizio utilizzato per avviare il server. Esegue questa operazione chiamando [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).

Il server è in grado di acquisire l'handle delle credenziali e di passare allo stato di ascolto oppure può attendere lo stato di ascolto fino a quando non arriva una richiesta di connessione e quindi acquisire un handle di credenziali in ingresso. Per ulteriori informazioni sulle funzioni di credenziali, vedere [gestione delle](authentication-functions.md)credenziali.

Quando il server riceve un messaggio di richiesta di connessione da un client, crea un [*contesto di sicurezza*](../secgloss/s-gly.md) locale per il client usando [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext). Il server usa questo contesto di sicurezza locale per eseguire richieste future dallo stesso client. Per ulteriori informazioni sulle funzioni di contesto, vedere [gestione del contesto](authentication-functions.md).

Il server controlla lo stato restituito e il descrittore del buffer di output per assicurarsi che non siano presenti errori fino a questo momento e può rifiutare la richiesta di connessione in caso di errori. Se sono presenti informazioni nel buffer di output restituito da [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), il buffer viene aggregato in un messaggio di risposta al client.

Qualsiasi buffer di output da [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) deve essere restituito al client. Inoltre, se lo stato di restituzione richiede che il protocollo continui (il secondo \_ \_ è stato \_ necessario o il secondo \_ \_ completamento \_ e \_ continua), è necessario un altro scambio di messaggi con il client.

Per le gambe aggiuntive, il server attende che il client risponda con un altro messaggio. Questa attesa può essere scaduta in modo da evitare un attacco Denial of Service in cui un client non risponde mai, causando un thread server e presto tutti i thread del server, per non rispondere.

 

 
