---
description: Il server invia al client un riferimento al contesto di sicurezza condiviso usando la direttiva opaca della richiesta digest.
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: Autenticazione delle richieste successive con Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25954612a99fa0a0a9710f5e8e0679948cc3bac5ceae669a06ec40bd5c22241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101426"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>Autenticazione delle richieste successive con Microsoft Digest

Il server invia al client un riferimento al contesto [*di sicurezza*](/windows/desktop/SecGloss/s-gly) condiviso usando la direttiva opaca della richiesta digest. Al termine dell'autenticazione, il client deve specificare questo valore nelle richieste successive al server di destinazione. L'inclusione del valore opaco nelle richieste di risorse accessibili tramite il contesto di sicurezza esistente elimina la necessità di eseguire nuovamente l'autenticazione nel controller di dominio. Tali richieste vengono autenticate nuovamente nel server, usando la chiave [*di sessione*](/windows/desktop/SecGloss/s-gly) digest memorizzata nella cache dopo l'autenticazione iniziale.

Il diagramma seguente illustra i passaggi esersi dal client e dal server durante una successiva richiesta di risorse protette dall'accesso.

![autenticazione di richieste successive tramite digest Microsoft](images/digest2.png)

Per richiedere risorse aggiuntive dopo un'autenticazione riuscita, il client chiama la Microsoft Digest [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per generare una risposta di richiesta digest. Il valore opaco è incluso nella direttiva opaca della risposta alla richiesta inviata al server come intestazione Authorization (visualizzata come richiesta HTTP).

Il server chiama la [**funzione AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) per determinare se esiste un contesto [*di sicurezza*](/windows/desktop/SecGloss/s-gly) per il client. Quando viene trovato un contesto esistente, la funzione restituisce SEC E COMPLETE NEEDED per indicare che il server deve \_ \_ chiamare la funzione \_ [**CompleteAuthToken.**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) Questa funzione esegue l'autenticazione client usando la [](initial-authentication-using-microsoft-digest.md) chiave [*di sessione*](/windows/desktop/SecGloss/s-gly) digest memorizzata nella cache durante l'autenticazione iniziale anziché eseguire nuovamente l'autenticazione nel controller di dominio.

 

 
