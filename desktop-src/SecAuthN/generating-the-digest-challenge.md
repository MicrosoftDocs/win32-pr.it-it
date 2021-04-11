---
description: La richiesta di Microsoft Digest viene generata dalla chiamata iniziale del server alla funzione AcceptSecurityContext (digest).
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: Generazione della richiesta digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511ec4f01c90acf08669835f9728cc711dfd1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233284"
---
# <a name="generating-the-digest-challenge"></a>Generazione della richiesta digest

La richiesta di Microsoft Digest viene generata dalla chiamata iniziale del server alla funzione [**AcceptSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Questa chiamata di funzione genera un parametro nonce, ovvero un valore univoco che contiene informazioni che possono essere utilizzate per rilevare le violazioni di sicurezza. Questa chiamata genera anche un [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) parziale usato per mantenere le informazioni sullo stato. Quando si chiama **AcceptSecurityContext (digest)** si specificano i flag dei requisiti di contesto per controllare il comportamento di Microsoft Digest e per impostare la qualità della protezione. Per altre informazioni, vedere [requisiti del contesto di richiesta digest](#digest-challenge-context-requirements).

L'output della chiamata iniziale alla [*funzione*](/windows/desktop/SecGloss/c-gly) [**AcceptSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) è un buffer di sicurezza che contiene un token inviato al client con una risposta HTTP 401 (accesso negato).

> [!Note]  
> Le chiamate a [**AcceptSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) che non contengono informazioni nei buffer di input restituiscono una richiesta di digest.

 

## <a name="digest-challenge-context-requirements"></a>Requisiti del contesto di richiesta digest

I requisiti di contesto sono flag che determinano:

-   Indica se Microsoft Digest funziona come meccanismo SASL o protocollo di autenticazione HTTP.
-   Qualità della protezione supportata dal contesto di sicurezza condiviso dal client e dal server.

Per impostazione predefinita, Microsoft Digest funziona come meccanismo SASL. Per usarlo per l'autenticazione HTTP, il \_ flag ASC req \_ http (0x10000000) deve essere impostato dal server.

I requisiti di contesto vengono specificati come flag passati al parametro *fContextReq* della funzione [**AcceptSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . I flag influiscono sulla qualità della protezione del contesto di sicurezza controllando la direttiva qop nella richiesta di verifica.

Per impostazione predefinita, la direttiva qop è impostata su "auth". Per generare una richiesta di verifica che imposta la direttiva qop su "auth-int", il server deve specificare uno o più dei flag seguenti:

-   integrità di ASC \_ req \_
-   \_ \_ rilevamento riesecuzione di ASC req \_
-   \_ \_ rilevamento sequenza ASC \_ req

Solo per SASL: generate una richiesta di verifica con la direttiva qop impostata su "auth-conf" specificando il \_ \_ flag di requisito del contesto di riservatezza ASC req. Poiché questo flag non è valido per l'autenticazione HTTP, non può essere usato con il \_ \_ flag http ASC req.

Per ulteriori informazioni sulla direttiva qop, vedere la pagina relativa alla [qualità della protezione e alle crittografie](quality-of-protection-and-ciphers.md).

Per ulteriori informazioni sulle problematiche, vedere la pagina relativa ai [contenuti di una richiesta digest](contents-of-a-digest-challenge.md).

 

 
