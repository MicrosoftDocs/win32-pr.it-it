---
description: Il server invia al client un riferimento al contesto di sicurezza condiviso usando la direttiva Opaque della richiesta digest.
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: Autenticazione delle richieste successive con Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eecccc3be68fb541994e63cdfc5035187e04aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758399"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>Autenticazione delle richieste successive con Microsoft Digest

Il server invia al client un riferimento al contesto di [*sicurezza*](/windows/desktop/SecGloss/s-gly) condiviso usando la direttiva Opaque della richiesta digest. Una volta completata l'autenticazione, il client deve specificare questo valore nelle richieste successive al server di destinazione. L'inclusione del valore opaco nelle richieste di risorse accessibili tramite il contesto di sicurezza esistente elimina la necessità di ripetere l'autenticazione nel controller di dominio. Tali richieste vengono nuovamente autenticate nel server, utilizzando la [*chiave della sessione*](/windows/desktop/SecGloss/s-gly) digest memorizzata nella cache dopo l'autenticazione iniziale.

Il diagramma seguente illustra i passaggi eseguiti da client e server durante una richiesta successiva per le risorse protette dall'accesso.

![autenticazione delle richieste successive tramite Microsoft Digest](images/digest2.png)

Per richiedere risorse aggiuntive dopo un'autenticazione corretta, il client chiama la funzione Microsoft Digest [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per generare una risposta di verifica del digest. Il valore opaco è incluso nella direttiva Opaque della risposta di richiesta di verifica inviata al server come intestazione di autorizzazione (visualizzata come richiesta HTTP).

Il server chiama la funzione [**AcceptSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) per determinare se esiste un contesto di [*sicurezza*](/windows/desktop/SecGloss/s-gly) esistente per il client. Quando viene trovato un contesto esistente, la funzione restituisce il secondo \_ E il \_ completamento \_ necessario per indicare che il server deve quindi chiamare la funzione [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) . Questa funzione esegue l'autenticazione client usando la [*chiave della sessione*](/windows/desktop/SecGloss/s-gly) digest memorizzata nella cache durante l' [autenticazione iniziale](initial-authentication-using-microsoft-digest.md) anziché eseguire di nuovo l'autenticazione nel controller di dominio.

 

 
