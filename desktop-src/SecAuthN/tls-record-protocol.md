---
description: Il protocollo di record Transport Layer Security (TLS) protegge i dati delle applicazioni usando le chiavi create durante l'handshake.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Protocollo di record TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316203"
---
# <a name="tls-record-protocol"></a>Protocollo di record TLS

Il protocollo di record [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) protegge i dati delle applicazioni usando le chiavi create durante l' [handshake](tls-handshake-protocol.md). Il protocollo di record è responsabile della protezione dei dati dell'applicazione e della verifica dell' [*integrità*](../secgloss/i-gly.md) e dell'origine. Gestisce gli elementi seguenti:

-   Dividere i messaggi in uscita in blocchi gestibili e riassemblare i messaggi in ingresso.
-   Compressione di blocchi in uscita e decompressione di blocchi in ingresso (facoltativo).
-   Applicare un [*Message Authentication Code*](../secgloss/m-gly.md) (Mac) ai messaggi in uscita e verificare i messaggi in arrivo tramite il Mac.
-   Crittografia dei messaggi in uscita e decrittografia dei messaggi in ingresso.

Una volta completato il protocollo di record, i dati crittografati in uscita vengono passati al livello Transmission Control Protocol (TCP) per il trasporto.

 

 
