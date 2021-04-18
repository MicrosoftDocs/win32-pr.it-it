---
description: Viene illustrato come stabilire un contesto di sicurezza che protegge le comunicazioni tra un client e un server.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Creazione di un contesto di sicurezza Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311940"
---
# <a name="creating-an-schannel-security-context"></a>Creazione di un contesto di sicurezza Schannel

Per stabilire un [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) che protegga le comunicazioni tra un client e un server, entrambi devono partecipare al processo di scambio di Informazioni seguente:

## <a name="client"></a>Client

1.  Il client chiama la funzione [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .
2.  Schannel inizia la creazione di un contesto di sicurezza in base alle regole del protocollo di sicurezza selezionato. Il codice restituito della funzione indica se il client deve chiamare di nuovo la funzione. [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) può restituire un token che rappresenta il contesto.
3.  Se è stato restituito un token, il client lo invia al server.
4.  Quando [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) restituisce sec \_ E \_ OK, il client viene eseguito. Se la funzione restituisce il \_ secondo \_ \_ , il client deve attendere che il server invii un token. Quando il client dispone del token dal server, deve chiamare di nuovo la [*funzione*](/windows/desktop/SecGloss/c-gly) **InitializeSecurityContext (General)** . (Tornare al passaggio 2).

## <a name="server"></a>Server

1.  Il server attende che un client invii un messaggio che contiene un token di sicurezza. Il server passa il token ricevuto dal client alla funzione [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
2.  Schannel si basa sul contesto di sicurezza parziale rappresentato dal token. Schannel restituisce un token al server e un codice restituito che indica se il server deve chiamare di nuovo la funzione.
3.  Se è stato restituito un token, il server lo invia al client.
4.  Quando [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) restituisce sec \_ E \_ OK, il server viene eseguito. Se la funzione restituisce il \_ secondo \_ \_ , l'utente continua a essere necessario, il server deve attendere che il client invii un token. Quando il server ha il token dal client, deve chiamare di nuovo la funzione **AcceptSecurityContext (generale)** . (Tornare al passaggio 2).

Se una delle due funzioni restituisce un valore diverso da SEC \_ e \_ OK, sec \_ I \_ continuerà a essere \_ necessario o sec \_ e \_ messaggio incompleto \_ (vedere il paragrafo seguente) si è verificato un errore. Il client e il server devono chiamare la funzione [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) per eliminare il contesto di sicurezza parzialmente stabilito.

Un caso speciale in cui è possibile modificare l'elaborazione del client e del server è quando al client o al server dell'altra parte vengono inviate troppe informazioni. Nel caso di informazioni troppo piccole, entrambe le funzioni restituiscono \_ un \_ messaggio incompleto al secondo E \_ . Per informazioni sul riconoscimento e la gestione di informazioni insufficienti o superflue, vedere [buffer aggiuntivi restituiti da Schannel](extra-buffers-returned-by-schannel.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione dell'autenticazione con Schannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Mapping dei certificati](mapping-certificates.md)
</dt> <dt>

[Convalida manuale di credenziali Schannel](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
