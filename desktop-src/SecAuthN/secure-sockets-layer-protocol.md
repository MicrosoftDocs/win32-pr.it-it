---
description: Le informazioni contenute in questo argomento si applicano a Windows Server 2003 e Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Protocollo Secure Sockets Layer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967386"
---
# <a name="secure-sockets-layer-protocol"></a>Protocollo Secure Sockets Layer

Le informazioni contenute in questo argomento si applicano a Windows Server 2003 e Windows XP. Per i pacchetti di crittografia per Windows Server 2008 e Windows Vista, vedere pacchetti [di crittografia in Schannel](cipher-suites-in-schannel.md).

Schannel supporta le versioni 2,0 e 3,0 del [*protocollo Secure Sockets Layer (SSL)*](../secgloss/s-gly.md).

> [!Note]  
> A partire da Windows 10, versione 1607 e Windows Server 2016, SSL 2,0 è stato rimosso e non è più supportato.

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3,0 è il predecessore del [protocollo Transport Layer Security](transport-layer-security-protocol.md).

Schannel supporta i pacchetti di crittografia elencati in pacchetti di [crittografia TLS](tls-cipher-suites.md) per SSL 3,0. SSL 3,0 supporta tutti i pacchetti di crittografia elencati in pacchetti di crittografia TLS e SSL \_ fortezza \_ Kea \_ con la \_ fortezza \_ CBC \_ Sha.

## <a name="ssl-20"></a>SSL 2.0

SSL 2,0 è stato sostituito da TLS e non deve essere usato per il nuovo sviluppo.

Schannel supporta i pacchetti di crittografia seguenti per SSL 2,0. I gruppi vengono elencati in ordine dal più sicuro al meno sicuro.

-   SSL \_ RC4 \_ 128 \_ con \_ MD5
-   SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5
-   SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ con \_ MD5
-   SSL \_ DES \_ 64 \_ CBC \_ con \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ con \_ MD5

 

 
