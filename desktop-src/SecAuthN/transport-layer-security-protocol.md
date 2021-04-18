---
description: Schannel supporta le versioni 1,0, 1,1 e 1,2 del protocollo Transport Layer Security (TLS).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocollo TLS (Transport Layer Security)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315858"
---
# <a name="transport-layer-security-protocol"></a>Protocollo TLS (Transport Layer Security)

Schannel supporta le versioni 1,0, 1,1 e 1,2 del [*protocollo Transport Layer Security (TLS)*](../secgloss/t-gly.md). Questo protocollo è uno standard di settore progettato per proteggere la privacy delle informazioni comunicate tramite Internet. TLS presuppone che sia in uso un trasporto orientato alla connessione, in genere TCP. Il protocollo TLS consente alle applicazioni client/server di rilevare i rischi di sicurezza seguenti:

-   Manomissione di messaggi
-   Intercettazione messaggi
-   Falsificazione del messaggio

La specifica completa del protocollo TLS è disponibile nel sito Web IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .

## <a name="organization-of-tls"></a>Organizzazione di TLS

Per l'uso di TLS per la comunicazione client/server sono necessari i passaggi seguenti:

 **Per usare TLS per la comunicazione client/server**

1.  Negoziazione di handshake e del pacchetto di crittografia
2.  Autenticazione delle entità
3.  Scambio di informazioni correlate alla chiave
4.  Scambio di dati dell'applicazione

I passaggi che costituiscono TLS sono divisi in due protocolli che, insieme, forniscono la sicurezza della connessione:

-   [Protocollo di handshake TLS](tls-handshake-protocol.md)-(passaggi da 1 a 3)
-   [Protocollo di record TLS](tls-record-protocol.md)-(passaggio 4)

## <a name="sspi-with-tls-implementations"></a>SSPI con implementazioni TLS

Poiché TLS non ha una specifica GSSAPI, i responsabili dell'implementazione di TLS potrebbero non avere familiarità con le funzioni SSPI. Le applicazioni chiamano le funzioni SSPI per enumerare i pacchetti disponibili, creare e utilizzare handle per le credenziali, creare contesti di sicurezza e garantire la privacy dell'integrità dei messaggi.

Per supportare le funzioni SSPI utilizzate dalle applicazioni in modalità utente, le funzioni elencate in [funzioni implementate da SSP/APS in modalità utente](/windows/desktop/SecAuthN/authentication-functions) devono essere supportate dalle implementazioni TLS, ad esempio schannel.dll.

Per informazioni dettagliate sulle funzioni SSPI e sulle funzioni SSP, vedere [funzioni di autenticazione](authentication-functions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pacchetti di crittografia TLS](tls-cipher-suites.md)
</dt> <dt>

[TLS e SSL](tls-versus-ssl.md)
</dt> </dl>

 

 
