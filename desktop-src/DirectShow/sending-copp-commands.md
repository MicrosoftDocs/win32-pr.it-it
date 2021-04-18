---
description: Invio di comandi COPP
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Invio di comandi COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303873"
---
# <a name="sending-copp-commands"></a><span data-ttu-id="8335f-103">Invio di comandi COPP</span><span class="sxs-lookup"><span data-stu-id="8335f-103">Sending COPP Commands</span></span>

<span data-ttu-id="8335f-104">Per inviare un comando COPP (Certified Output Protocol), compilare una struttura [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8335f-104">To send a Certified Output Protection Protocol (COPP) command, fill in an [**AMCOPPCommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) structure as follows:</span></span>

-   <span data-ttu-id="8335f-105">**guidCommandID**.</span><span class="sxs-lookup"><span data-stu-id="8335f-105">**guidCommandID**.</span></span> <span data-ttu-id="8335f-106">GUID che identifica il comando.</span><span class="sxs-lookup"><span data-stu-id="8335f-106">The GUID that identifies the command.</span></span> <span data-ttu-id="8335f-107">Vedere le informazioni di riferimento sui comandi di COPP.</span><span class="sxs-lookup"><span data-stu-id="8335f-107">See the COPP Command Reference.</span></span>
-   <span data-ttu-id="8335f-108">**dwSequence**.</span><span class="sxs-lookup"><span data-stu-id="8335f-108">**dwSequence**.</span></span> <span data-ttu-id="8335f-109">Numero di sequenza del comando.</span><span class="sxs-lookup"><span data-stu-id="8335f-109">The command sequence number.</span></span> <span data-ttu-id="8335f-110">Incrementare questo valore dopo ogni comando.</span><span class="sxs-lookup"><span data-stu-id="8335f-110">Increment this value after each command.</span></span> <span data-ttu-id="8335f-111">Questo valore viene visualizzato come **uCommandSeq** durante [l'avvio di una sessione COPP](initiating-a-copp-session.md).</span><span class="sxs-lookup"><span data-stu-id="8335f-111">(This value is shown as **uCommandSeq** in [Initiating a COPP Session](initiating-a-copp-session.md).)</span></span>
-   <span data-ttu-id="8335f-112">**cbSizeData**.</span><span class="sxs-lookup"><span data-stu-id="8335f-112">**cbSizeData**.</span></span> <span data-ttu-id="8335f-113">Dimensione, in byte, dei dati necessari per il comando.</span><span class="sxs-lookup"><span data-stu-id="8335f-113">The size, in bytes, of any data needed for the command.</span></span>
-   <span data-ttu-id="8335f-114">**CommandData**.</span><span class="sxs-lookup"><span data-stu-id="8335f-114">**CommandData**.</span></span> <span data-ttu-id="8335f-115">Dati per il comando.</span><span class="sxs-lookup"><span data-stu-id="8335f-115">Data for the command.</span></span>

<span data-ttu-id="8335f-116">Dopo aver compilato i dati, calcolare il MAC per il comando:</span><span class="sxs-lookup"><span data-stu-id="8335f-116">After you have filled in this data, calculate the MAC for the command:</span></span>

1.  <span data-ttu-id="8335f-117">Calcolare il tag OMAC-1 per il blocco di dati visualizzato dopo il membro **macKDI** della struttura **AMCOPPCommand** .</span><span class="sxs-lookup"><span data-stu-id="8335f-117">Calculate the OMAC-1 tag for the block of data that appears after the **macKDI** member of the **AMCOPPCommand** structure.</span></span>
2.  <span data-ttu-id="8335f-118">Copiare questo valore nel membro **macKDI** della struttura.</span><span class="sxs-lookup"><span data-stu-id="8335f-118">Copy this value into the **macKDI** member of the structure.</span></span>

<span data-ttu-id="8335f-119">Passare quindi la struttura al metodo [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) .</span><span class="sxs-lookup"><span data-stu-id="8335f-119">Now pass the structure to the [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8335f-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8335f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8335f-121">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="8335f-121">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



