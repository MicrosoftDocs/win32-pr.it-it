---
description: Riferimento al comando COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Riferimento al comando COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304328"
---
# <a name="copp-command-reference"></a><span data-ttu-id="da134-103">Riferimento al comando COPP</span><span class="sxs-lookup"><span data-stu-id="da134-103">COPP Command Reference</span></span>

<span data-ttu-id="da134-104">In questa sezione vengono descritti i comandi COPP (Certified Output Protocol).</span><span class="sxs-lookup"><span data-stu-id="da134-104">This section describes the Certified Output Protection Protocol (COPP) commands.</span></span> <span data-ttu-id="da134-105">Vengono definiti i comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="da134-105">The following commands are defined.</span></span>



| <span data-ttu-id="da134-106">Comando</span><span class="sxs-lookup"><span data-stu-id="da134-106">Command</span></span>              | <span data-ttu-id="da134-107">GUID</span><span class="sxs-lookup"><span data-stu-id="da134-107">GUID</span></span>                             |
|----------------------|----------------------------------|
| <span data-ttu-id="da134-108">Imposta il livello di protezione</span><span class="sxs-lookup"><span data-stu-id="da134-108">Set Protection Level</span></span> | <span data-ttu-id="da134-109">**\_COPPSETPROTECTIONLEVEL DXVA**</span><span class="sxs-lookup"><span data-stu-id="da134-109">**DXVA\_COPPSetProtectionLevel**</span></span> |
| <span data-ttu-id="da134-110">Imposta segnalazione</span><span class="sxs-lookup"><span data-stu-id="da134-110">Set Signaling</span></span>        | <span data-ttu-id="da134-111">**\_COPPSETSIGNALING DXVA**</span><span class="sxs-lookup"><span data-stu-id="da134-111">**DXVA\_COPPSetSignaling**</span></span>       |



 

<span data-ttu-id="da134-112">Comando Imposta livello di protezione</span><span class="sxs-lookup"><span data-stu-id="da134-112">Set Protection Level Command</span></span>

<span data-ttu-id="da134-113">Imposta il livello di protezione per un meccanismo di protezione dell'output specificato.</span><span class="sxs-lookup"><span data-stu-id="da134-113">Sets the protection level for a specified output protection mechanism.</span></span> <span data-ttu-id="da134-114">A seconda del connettore, potrebbe essere possibile applicare più di un meccanismo di protezione sullo stesso connettore, con impostazioni diverse per ogni meccanismo.</span><span class="sxs-lookup"><span data-stu-id="da134-114">Depending on the connector, it might be possible to apply more than one protection mechanism on the same connector, with different settings for each mechanism.</span></span>

<span data-ttu-id="da134-115">**GUID**: DXVA \_ COPPSetProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="da134-115">**GUID**: DXVA\_COPPSetProtectionLevel</span></span>

<span data-ttu-id="da134-116">**Dati di input**: [**struttura \_ COPPSetProtectionLevelCmdData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .</span><span class="sxs-lookup"><span data-stu-id="da134-116">**Input data**: A [**DXVA\_COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) structure.</span></span>

<span data-ttu-id="da134-117">Imposta comando di segnalazione</span><span class="sxs-lookup"><span data-stu-id="da134-117">Set Signaling Command</span></span>

<span data-ttu-id="da134-118">Specifica informazioni sul segnale video diverso dal livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="da134-118">Specifies information about the video signal other than the protection level.</span></span>

<span data-ttu-id="da134-119">Per CGMS-A, determinati standard di protezione richiedono che il segnale Televsion contenga informazioni sulle proporzioni e altre informazioni all'interno degli stessi pacchetti di forme d'onda VBI dei bit CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="da134-119">For CGMS-A, certain protection standards require that the televsion signal contains information about the aspect ratio and other information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="da134-120">I televisori potrebbero non essere visualizzati correttamente se le informazioni sulle proporzioni non sono coerenti con il flusso video.</span><span class="sxs-lookup"><span data-stu-id="da134-120">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="da134-121">L'applicazione può utilizzare questo comando per specificare le proporzioni in modo che il driver di grafica possa generare i pacchetti VBI corretti.</span><span class="sxs-lookup"><span data-stu-id="da134-121">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

<span data-ttu-id="da134-122">Questo comando è anche progettato per essere estendibile se sono necessarie informazioni aggiuntive sul segnale negli standard futuri.</span><span class="sxs-lookup"><span data-stu-id="da134-122">This command is also designed to be extensible if additional signal information is required in future standards.</span></span>

<span data-ttu-id="da134-123">**GUID**: DXVA \_ COPPSetSignaling</span><span class="sxs-lookup"><span data-stu-id="da134-123">**GUID**: DXVA\_COPPSetSignaling</span></span>

<span data-ttu-id="da134-124">**Dati di input**: [**struttura \_ COPPSetSignalingCmdData di DXVA**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="da134-124">**Input data**: A [**DXVA\_COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da134-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da134-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da134-126">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="da134-126">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



