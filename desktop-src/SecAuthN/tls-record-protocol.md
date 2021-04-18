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
# <a name="tls-record-protocol"></a><span data-ttu-id="09dd8-103">Protocollo di record TLS</span><span class="sxs-lookup"><span data-stu-id="09dd8-103">TLS Record Protocol</span></span>

<span data-ttu-id="09dd8-104">Il protocollo di record [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) protegge i dati delle applicazioni usando le chiavi create durante l' [handshake](tls-handshake-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="09dd8-104">The [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Record protocol secures application data using the keys created during the [Handshake](tls-handshake-protocol.md).</span></span> <span data-ttu-id="09dd8-105">Il protocollo di record è responsabile della protezione dei dati dell'applicazione e della verifica dell' [*integrità*](../secgloss/i-gly.md) e dell'origine.</span><span class="sxs-lookup"><span data-stu-id="09dd8-105">The Record Protocol is responsible for securing application data and verifying its [*integrity*](../secgloss/i-gly.md) and origin.</span></span> <span data-ttu-id="09dd8-106">Gestisce gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="09dd8-106">It manages the following:</span></span>

-   <span data-ttu-id="09dd8-107">Dividere i messaggi in uscita in blocchi gestibili e riassemblare i messaggi in ingresso.</span><span class="sxs-lookup"><span data-stu-id="09dd8-107">Dividing outgoing messages into manageable blocks, and reassembling incoming messages.</span></span>
-   <span data-ttu-id="09dd8-108">Compressione di blocchi in uscita e decompressione di blocchi in ingresso (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="09dd8-108">Compressing outgoing blocks and decompressing incoming blocks (optional).</span></span>
-   <span data-ttu-id="09dd8-109">Applicare un [*Message Authentication Code*](../secgloss/m-gly.md) (Mac) ai messaggi in uscita e verificare i messaggi in arrivo tramite il Mac.</span><span class="sxs-lookup"><span data-stu-id="09dd8-109">Applying a [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) to outgoing messages, and verifying incoming messages using the MAC.</span></span>
-   <span data-ttu-id="09dd8-110">Crittografia dei messaggi in uscita e decrittografia dei messaggi in ingresso.</span><span class="sxs-lookup"><span data-stu-id="09dd8-110">Encrypting outgoing messages and decrypting incoming messages.</span></span>

<span data-ttu-id="09dd8-111">Una volta completato il protocollo di record, i dati crittografati in uscita vengono passati al livello Transmission Control Protocol (TCP) per il trasporto.</span><span class="sxs-lookup"><span data-stu-id="09dd8-111">When the Record Protocol is complete, the outgoing encrypted data is passed down to the Transmission Control Protocol (TCP) layer for transport.</span></span>

 

 
