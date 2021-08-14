---
description: Le informazioni contenute in questo argomento si applicano Windows Server 2003 e Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: protocollo Secure Sockets Layer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8e6b7232db8bef98d5170887d6be75c9770927954a40b606450bf214efdf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918384"
---
# <a name="secure-sockets-layer-protocol"></a>protocollo Secure Sockets Layer

Le informazioni contenute in questo argomento si applicano Windows Server 2003 e Windows XP. Per i pacchetti di crittografia per Windows Server 2008 e Windows Vista, vedere Pacchetti di [crittografia in Schannel.](cipher-suites-in-schannel.md)

Schannel supporta le versioni 2.0 e 3.0 [*del protocollo Secure Sockets Layer (SSL).*](../secgloss/s-gly.md)

> [!Note]  
> A partire Windows 10 versione 1607 e Windows Server 2016, SSL 2.0 è stato rimosso e non è più supportato.

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3.0 è il predecessore del [protocollo Transport Layer Security.](transport-layer-security-protocol.md)

Schannel supporta i pacchetti di crittografia elencati in [Pacchetti di crittografia TLS](tls-cipher-suites.md) per SSL 3.0. SSL 3.0 supporta tutti i pacchetti di crittografia elencati in TLS Cipher Suites (Pacchetti di crittografia TLS) e SSL \_ FORQUAL \_ KEA WITH FORQUAL CBC SHA (SSL FORNELLA KEA \_ WITH \_ FORATURA \_ CBC \_ SHA).

## <a name="ssl-20"></a>SSL 2.0

SSL 2.0 è stato sostituito da TLS e non deve essere usato per il nuovo sviluppo.

Schannel supporta i pacchetti di crittografia seguenti per SSL 2.0. Le suite sono elencate nell'ordine dal più sicuro al meno sicuro.

-   SSL \_ RC4 \_ 128 \_ WITH \_ MD5
-   SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ WITH \_ MD5
-   SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ CON \_ MD5
-   SSL \_ DES \_ 64 \_ CBC CON \_ \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ WITH \_ MD5

 

 
