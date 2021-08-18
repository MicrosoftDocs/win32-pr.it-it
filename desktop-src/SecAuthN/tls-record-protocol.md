---
description: Il protocollo Transport Layer Security (TLS) Record protegge i dati dell'applicazione usando le chiavi create durante l'handshake.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Protocollo di record TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce441de892367b49e1fd4aa285b5398dd5e7c1667d0ea785f6925995c89e1dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915741"
---
# <a name="tls-record-protocol"></a>Protocollo di record TLS

Il [*protocollo Transport Layer Security*](../secgloss/t-gly.md) (TLS) Record protegge i dati dell'applicazione usando le chiavi create durante [l'handshake.](tls-handshake-protocol.md) Il protocollo di registrazione è responsabile della protezione dei dati dell'applicazione e della verifica [*dell'integrità e*](../secgloss/i-gly.md) dell'origine. Gestisce gli elementi seguenti:

-   Divisione dei messaggi in uscita in blocchi gestibili e riassemblamento dei messaggi in ingresso.
-   Compressione dei blocchi in uscita e decompressione dei blocchi in ingresso (facoltativo).
-   Applicazione di un [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) ai messaggi in uscita e verifica dei messaggi in ingresso tramite MAC.
-   Crittografia dei messaggi in uscita e decrittografia dei messaggi in ingresso.

Al termine del protocollo di registrazione, i dati crittografati in uscita vengono passati al livello Transmission Control Protocol (TCP) per il trasporto.

 

 
