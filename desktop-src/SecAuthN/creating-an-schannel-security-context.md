---
description: Viene illustrato come stabilire un contesto di sicurezza che protegga le comunicazioni tra un client e un server.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Creazione di un contesto di sicurezza Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7373d2ed4f8cc385a2245e6971f8233aad052930d4995225abfda8eab0191aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008859"
---
# <a name="creating-an-schannel-security-context"></a>Creazione di un contesto di sicurezza Schannel

Per stabilire un [*contesto di sicurezza che*](/windows/desktop/SecGloss/s-gly) proteggerà le comunicazioni tra un client e un server, entrambi devono partecipare al processo di scambio di informazioni seguente:

## <a name="client"></a>Client

1.  Il client chiama la [**funzione InitializeSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
2.  Schannel inizia a creare un contesto di sicurezza in base alle regole del protocollo di sicurezza selezionato. Il codice restituito della funzione indica se il client deve chiamare nuovamente la funzione. [**InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) può restituire un token che rappresenta il contesto.
3.  Se è stato restituito un token, il client lo invia al server.
4.  Quando [**InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) restituisce SEC \_ E \_ OK, il client viene eseguito. Se la funzione restituisce SEC I CONTINUE NEEDED, il client deve \_ attendere che il server \_ \_ invii un token. Quando il client ha il token dal server, deve chiamare nuovamente la funzione **InitializeSecurityContext (General).** [](/windows/desktop/SecGloss/c-gly) Tornare al passaggio 2.

## <a name="server"></a>Server

1.  Il server attende che un client invii un messaggio contenente un token di sicurezza. Il server passa il token ricevuto dal client alla [**funzione AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
2.  Schannel si basa sul contesto di sicurezza parziale rappresentato dal token. Schannel restituisce un token al server e un codice restituito che indica se il server deve chiamare di nuovo la funzione.
3.  Se è stato restituito un token, il server lo invia al client.
4.  Quando [**AcceptSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) restituisce SEC \_ E \_ OK, il server viene eseguito. Se la funzione restituisce SEC I CONTINUE NEEDED, il server deve attendere che \_ il client \_ \_ invii un token. Quando il server ha il token dal client, deve chiamare nuovamente la funzione **AcceptSecurityContext (General).** Tornare al passaggio 2.

Se una delle funzioni restituisce un valore diverso da SEC E OK, SEC I CONTINUE NEEDED o \_ SEC E \_ \_ \_ \_ \_ \_ INCOMPLETE MESSAGE (vedere il \_ paragrafo seguente) si è verificato un errore. Il client e il server devono chiamare la [**funzione DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) per eliminare il contesto di sicurezza parzialmente stabilito.

Un caso speciale che può modificare l'elaborazione client e server si verifica quando al client o al server vengono inviate informazioni troppo piccole o troppe dall'altra parte. Nel caso di informazioni troppo piccole, entrambe le funzioni restituiscono SEC \_ E \_ INCOMPLETE \_ MESSAGE. Per informazioni sul riconoscimento e sulla gestione di informazioni insufficienti o in eccesso, vedere [Buffer aggiuntivi restituiti da Schannel.](extra-buffers-returned-by-schannel.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione dell'autenticazione tramite Schannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Mapping dei certificati](mapping-certificates.md)
</dt> <dt>

[Convalida manuale delle credenziali Schannel](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
