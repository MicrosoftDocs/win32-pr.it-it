---
description: Le funzioni seguenti vengono utilizzate con l'output Protection Manager (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Funzioni di OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309065"
---
# <a name="opm-functions"></a><span data-ttu-id="da428-103">Funzioni di OPM</span><span class="sxs-lookup"><span data-stu-id="da428-103">OPM Functions</span></span>

<span data-ttu-id="da428-104">Le funzioni seguenti vengono utilizzate con l' [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="da428-104">The following functions are used with [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>



| <span data-ttu-id="da428-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="da428-105">Function</span></span>                                                                                             | <span data-ttu-id="da428-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da428-106">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da428-107">**OPMGetVideoOutputForTarget**</span><span class="sxs-lookup"><span data-stu-id="da428-107">**OPMGetVideoOutputForTarget**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | <span data-ttu-id="da428-108">Restituisce un oggetto di output video per la destinazione VidPN sull'adapter specificato.</span><span class="sxs-lookup"><span data-stu-id="da428-108">Returns a video output object for the VidPN target on the specified adapter.</span></span>                                                          |
| [<span data-ttu-id="da428-109">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="da428-109">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | <span data-ttu-id="da428-110">Crea un oggetto di gestione della protezione di output (OPM) per ogni monitoraggio fisico associato a un particolare handle **HMONITOR** .</span><span class="sxs-lookup"><span data-stu-id="da428-110">Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular **HMONITOR** handle.</span></span> |
| [<span data-ttu-id="da428-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="da428-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | <span data-ttu-id="da428-112">Crea un oggetto OPM per ogni monitoraggio fisico associato a un particolare dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="da428-112">Creates an OPM object for each physical monitor that is associated with a particular Direct3D device.</span></span>                                 |



 

<span data-ttu-id="da428-113">Le funzioni seguenti vengono usate da OPM per accedere alla funzionalità nel driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="da428-113">The following functions are used by OPM to access functionality in the display driver.</span></span> <span data-ttu-id="da428-114">Le applicazioni non devono chiamare queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="da428-114">Applications should not call these functions.</span></span>

-   [<span data-ttu-id="da428-115">**ConfigureOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="da428-115">**ConfigureOPMProtectedOutput**</span></span>](configureopmprotectedoutput.md)
-   [<span data-ttu-id="da428-116">**CreateOPMProtectedOutputs**</span><span class="sxs-lookup"><span data-stu-id="da428-116">**CreateOPMProtectedOutputs**</span></span>](createopmprotectedoutputs.md)
-   [<span data-ttu-id="da428-117">**DestroyOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="da428-117">**DestroyOPMProtectedOutput**</span></span>](destroyopmprotectedoutput.md)
-   [<span data-ttu-id="da428-118">**GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="da428-118">**GetCertificate**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [<span data-ttu-id="da428-119">**GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="da428-119">**GetCertificateSize**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [<span data-ttu-id="da428-120">**GetCOPPCompatibleOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="da428-120">**GetCOPPCompatibleOPMInformation**</span></span>](getcoppcompatibleopminformation.md)
-   [<span data-ttu-id="da428-121">**GetOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="da428-121">**GetOPMInformation**</span></span>](getopminformation.md)
-   [<span data-ttu-id="da428-122">**GetOPMRandomNumber**</span><span class="sxs-lookup"><span data-stu-id="da428-122">**GetOPMRandomNumber**</span></span>](getopmrandomnumber.md)
-   [<span data-ttu-id="da428-123">**GetSuggestedOPMProtectedOutputArraySize**</span><span class="sxs-lookup"><span data-stu-id="da428-123">**GetSuggestedOPMProtectedOutputArraySize**</span></span>](getsuggestedopmprotectedoutputarraysize.md)
-   [<span data-ttu-id="da428-124">**SetOPMSigningKeyAndSequenceNumbers**</span><span class="sxs-lookup"><span data-stu-id="da428-124">**SetOPMSigningKeyAndSequenceNumbers**</span></span>](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a><span data-ttu-id="da428-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da428-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da428-126">Guida di riferimento alla programmazione di OPM</span><span class="sxs-lookup"><span data-stu-id="da428-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="da428-127">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="da428-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



