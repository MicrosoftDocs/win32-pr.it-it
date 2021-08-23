---
description: Schannel supporta le versioni 1.0, 1.1 e 1.2 del protocollo Transport Layer Security (TLS).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocollo TLS (Transport Layer Security)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed6bc76b6a491105607c3110cda32723bbba75fdf55abe97f7667f397060209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915593"
---
# <a name="transport-layer-security-protocol"></a>Protocollo TLS (Transport Layer Security)

Schannel supporta le versioni 1.0, 1.1 e 1.2 del [*protocollo Transport Layer Security (TLS).*](../secgloss/t-gly.md) Questo protocollo è uno standard di settore progettato per proteggere la privacy delle informazioni durante la comunicazione tramite Internet. TLS presuppone che sia in uso un trasporto orientato alla connessione, in genere TCP. Il protocollo TLS consente alle applicazioni client/server di rilevare i rischi di sicurezza seguenti:

-   Manomissione dei messaggi
-   Intercettazione di messaggi
-   Contraffazione di messaggi

La specifica completa del protocollo TLS è disponibile nel sito Web IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .

## <a name="organization-of-tls"></a>Organizzazione di TLS

I passaggi seguenti riguardano l'uso di TLS per la comunicazione client/server:

 **Per usare TLS per la comunicazione client/server**

1.  Negoziazione di handshake e pacchetti di crittografia
2.  Autenticazione delle parti
3.  Scambio di informazioni relative alle chiavi
4.  Scambio di dati delle applicazioni

I passaggi che costituiscono TLS sono suddivisi in due protocolli che, insieme, forniscono la sicurezza della connessione:

-   [Protocollo handshake TLS](tls-handshake-protocol.md): (passaggi da 1 a 3)
-   [Protocollo di record TLS](tls-record-protocol.md)- (passaggio 4)

## <a name="sspi-with-tls-implementations"></a>SSPI con implementazioni TLS

Poiché TLS non ha una specifica GSSAPI, gli implementatori TLS potrebbero non avere familiarità con le funzioni SSPI. Le applicazioni chiamano le funzioni SSPI per enumerare i pacchetti disponibili, creare e usare handle alle credenziali, creare contesti di sicurezza e garantire la privacy dell'integrità dei messaggi.

Per supportare le funzioni SSPI usate dalle applicazioni in modalità utente, le funzioni elencate in Funzioni implementate da provider di servizi di [configurazione/provider](/windows/desktop/SecAuthN/authentication-functions) di servizi di configurazione in modalità utente devono essere supportate dalle implementazioni TLS, ad esempio schannel.dll.

Per informazioni dettagliate sulle funzioni SSPI e SSP, vedere [Funzioni di autenticazione.](authentication-functions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pacchetti di crittografia TLS](tls-cipher-suites.md)
</dt> <dt>

[TLS e SSL](tls-versus-ssl.md)
</dt> </dl>

 

 
