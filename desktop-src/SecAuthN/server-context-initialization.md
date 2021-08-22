---
description: Analogamente al client, il server acquisisce anche un handle di credenziali per essere pronto a rispondere a una richiesta di autenticazione in ingresso dal client.
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: Inizializzazione del contesto del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d4a81c8033dc6b5dda8baca9ee7dfcc87d2b14c1cd139ff4a7f8eda99603f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918330"
---
# <a name="server-context-initialization"></a>Inizializzazione del contesto del server

Analogamente al client, il server acquisisce anche un [*handle*](../secgloss/c-gly.md) di credenziali per essere pronto a rispondere a una richiesta di autenticazione in ingresso dal client. Le credenziali del server vengono utilizzate per autenticare il server nel client [*nei*](../secgloss/s-gly.md) protocolli di sicurezza che supportano l'autenticazione server o l'autenticazione reciproca. Il server ottiene un handle per le credenziali definite dall'account del servizio utilizzato per avviare il server. A tale scopo, chiama [**AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)

Il server può acquisire l'handle delle credenziali e quindi passare a uno stato di ascolto oppure può attendere in uno stato di ascolto fino all'arrivo di una richiesta di connessione e quindi acquisire un handle di credenziali in ingresso. Per altre informazioni sulle funzioni delle credenziali, vedere [Gestione delle credenziali.](authentication-functions.md)

Quando il server riceve un messaggio di richiesta di [](../secgloss/s-gly.md) connessione da un client, crea un contesto di sicurezza locale per il client usando [**AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Il server usa questo contesto di sicurezza locale per eseguire richieste future da parte dello stesso client. Per altre informazioni sulle funzioni di contesto, vedere [Gestione del contesto.](authentication-functions.md)

Il server controlla lo stato restituito e il descrittore del buffer di output per assicurarsi che non siano presenti errori fino a questo momento e può rifiutare la richiesta di connessione in caso di errori. Se sono presenti informazioni nel buffer di output restituito da [**AcceptSecurityContext (Generale),**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)il buffer viene aggregato in un messaggio di risposta al client.

Qualsiasi buffer di output [**da AcceptSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) deve essere restituito al client. Inoltre, se lo stato restituito richiede che il protocollo continui (SEC I CONTINUE NEEDED o SEC I COMPLETE AND CONTINUE), è necessario un altro \_ scambio di messaggi con il \_ \_ \_ \_ \_ \_ client.

Per ulteriori operazioni, il server attende che il client risponda con un altro messaggio. Questa attesa può essere timeout in modo da evitare un attacco Denial of Service in cui un client non risponde di proposito, causando un thread del server e presto tutti i thread del server smetteranno di rispondere.

 

 
