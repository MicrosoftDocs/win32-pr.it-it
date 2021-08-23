---
description: La Microsoft Digest richiesta viene generata dalla chiamata iniziale del server alla funzione AcceptSecurityContext (Digest).
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: Generazione della richiesta digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a01a7edfa6498ed621e351c114e65a6d4ff6ef7a75b459cb29e00f0dc668a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623331"
---
# <a name="generating-the-digest-challenge"></a>Generazione della richiesta digest

La Microsoft Digest richiesta viene generata dalla chiamata iniziale del server alla [**funzione AcceptSecurityContext (Digest).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Questa chiamata di funzione genera un valore nonce, ovvero un valore univoco che contiene informazioni che possono essere usate per rilevare le violazioni della sicurezza. Questa chiamata genera anche un contesto [*di sicurezza*](/windows/desktop/SecGloss/s-gly) parziale usato per gestire le informazioni sullo stato. Quando si **chiama AcceptSecurityContext (Digest)** si specificano i flag dei requisiti di contesto per controllare il comportamento Microsoft Digest e per impostare la qualità della protezione. Per altre informazioni, vedere [Requisiti del contesto di richiesta digest](#digest-challenge-context-requirements).

L'output della chiamata iniziale alla funzione [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) [](/windows/desktop/SecGloss/c-gly) è un buffer di sicurezza che contiene un token inviato al client con una risposta HTTP 401 (accesso negato).

> [!Note]  
> Le chiamate [**ad AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) che non contengono informazioni nei buffer di input restituiscono una richiesta digest.

 

## <a name="digest-challenge-context-requirements"></a>Requisiti del contesto di richiesta digest

I requisiti di contesto sono flag che determinano:

-   Indica Microsoft Digest funziona come meccanismo SASL o protocollo di autenticazione HTTP.
-   Qualità della protezione supportata dal contesto di sicurezza condiviso dal client e dal server.

Per impostazione predefinita, Microsoft Digest come meccanismo SASL. Per usarlo per l'autenticazione HTTP, il flag ASC \_ REQ \_ HTTP (0x10000000) deve essere impostato dal server.

I requisiti di contesto vengono specificati come flag passati al *parametro fContextReq* della [**funzione AcceptSecurityContext (Digest).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) I flag influiscono sulla qualità della protezione del contesto di sicurezza controllando la direttiva qop nella richiesta.

Per impostazione predefinita, la direttiva qop è impostata su "auth". Per generare una richiesta di richiesta che imposta la direttiva qop su "auth-int", il server deve specificare uno o più dei flag seguenti:

-   INTEGRITÀ DEL \_ REQ ASC \_
-   ASC \_ REQ \_ REPLAY \_ DETECT
-   ASC \_ REQ \_ SEQUENCE \_ DETECT

Solo per SASL: generare una richiesta di verifica con la direttiva qop impostata su "auth-conf" specificando il flag del requisito di contesto ASC \_ REQ \_ CONFIDENTIALITY. Poiché questo flag non è valido per l'autenticazione HTTP, non può essere usato con il flag HTTP ASC \_ \_ REQ.

Per altre informazioni sulla direttiva qop, vedere [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).

Per altre informazioni sulle problematiche, vedere [Contenuto di una richiesta digest](contents-of-a-digest-challenge.md).

 

 
