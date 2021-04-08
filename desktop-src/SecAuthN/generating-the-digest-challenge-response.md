---
description: Dopo la ricezione di una richiesta di verifica da parte del server, il client crea la risposta di verifica del digest chiamando la funzione InitializeSecurityContext (digest).
ms.assetid: b26b5676-a614-4017-a4e5-a5395292a667
title: Generazione della risposta alla richiesta digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b577334348745425db23d3de41431ba4e37b7af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884521"
---
# <a name="generating-the-digest-challenge-response"></a>Generazione della risposta alla richiesta digest

Dopo la ricezione di una richiesta di verifica da parte del server, il client crea la risposta di verifica del digest chiamando la funzione [**InitializeSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Questa funzione genera un'impronta digitale MD5 [*hash*](/windows/desktop/SecGloss/h-gly) usando le informazioni sulla risorsa e sui dati richiesti dalla richiesta di verifica e restituisce un token di sicurezza che rappresenta un [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly)parziale. Per completare l'autenticazione, il client deve restituire il token al server che ha emesso la richiesta di verifica.

Nella tabella seguente vengono descritti i parametri della [*funzione*](/windows/desktop/SecGloss/c-gly) [**InitializeSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e i valori da fornire quando si costruisce una risposta di verifica del digest.



| Parametro                  | Descrizione                                                                                                                                                                                               |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *fContextReq*<br/>   | Attributi del contesto di sicurezza richiesti dal client. Per altre informazioni, vedere requisiti del contesto della risposta di richiesta digest.<br/>                                                             |
| *pszTargetName*<br/> | HTTP: stringa con terminazione null che specifica l'URL di destinazione.<br/> SASL: stringa con terminazione null che specifica la destinazione DNS/SPN.<br/>                                                         |
| *pInput*<br/>        | Buffer che contengono le informazioni richieste dal provider SSP del digest. Per altre informazioni, vedere [buffer di input per la risposta alla richiesta di verifica del digest](input-buffers-for-the-digest-challenge-response.md).<br/> |
| *pfContextAttr*<br/> | Riceve gli attributi supportati dal contesto di sicurezza restituito. Per altre informazioni, vedere requisiti del contesto della risposta di richiesta digest.<br/>                                                  |
| *pOutput*<br/>       | Indirizzo di un \_ buffer di tipo token SECBUFFER che riceve un token di sicurezza da restituire al server.<br/>                                                                                           |



 

## <a name="digest-challenge-response-context-requirements"></a>Requisiti del contesto della risposta di richiesta digest

I requisiti di contesto sono flag che determinano:

-   Indica se Microsoft Digest funziona come meccanismo SASL o protocollo di autenticazione HTTP.
-   Qualità della protezione supportata dal contesto di [*sicurezza*](/windows/desktop/SecGloss/s-gly) condiviso dal client e dal server.

Per impostazione predefinita, Microsoft Digest funziona come meccanismo SASL.

I requisiti di contesto vengono specificati come flag passati al parametro *fContextReq* della funzione [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . I flag influiscono sulla qualità della protezione del contesto di sicurezza controllando la direttiva qop nella risposta alla richiesta di verifica.

Per impostazione predefinita, la direttiva qop è impostata su "auth". Per generare una risposta di verifica che imposta qop su "auth-int", deve verificarsi quanto segue:

1.  La richiesta digest deve avere una direttiva qop impostata su "auth-int".
2.  Il client deve specificare uno o più dei flag seguenti:

    -   \_integrità req di ISC \_
    -   \_ \_ rilevamento riesecuzione richieste \_ ISC
    -   \_ \_ rilevamento sequenza req di ISC \_

Solo per SASL: generare una risposta di verifica con la direttiva qop impostata su "auth-conf" specificando il \_ \_ flag di riservatezza di ISC. Poiché questo flag non è valido per l'autenticazione HTTP, non può essere usato con il \_ flag http di richiesta ISC \_ .

## <a name="verifying-the-quality-of-protection"></a>Verifica della qualità della protezione

Il client deve esaminare i flag degli attributi del contesto di sicurezza restituiti nel parametro *pfContextAttr* della funzione [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Il client deve inviare la risposta alla richiesta di verifica al server solo se la qualità della protezione indicata dai flag è sufficiente per gli scopi. I flag rilevanti possono essere costituiti da qualsiasi combinazione dei seguenti elementi:

-   \_integrità RET di ISC \_
-   \_ \_ rilevamento riproduzione RET di \_ ISC
-   \_ \_ rilevamento sequenza RET di ISC \_
-   \_ \_ Riservatezza RET ISC (solo contesti SASL)

Per ulteriori informazioni sulla direttiva qop, vedere la pagina relativa alla [qualità della protezione e alle crittografie](quality-of-protection-and-ciphers.md).

Per ulteriori informazioni sulle direttive di risposta alla richiesta di verifica, vedere [contenuto di una risposta di verifica del digest](contents-of-a-digest-challenge-response.md).

 

