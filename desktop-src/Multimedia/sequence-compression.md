---
title: Compressione sequenza
description: Compressione sequenza
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- Gestione compressione video (VCM), compressione sequenza
- VCM (Video Compression Manager), compressione sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955418"
---
# <a name="sequence-compression"></a><span data-ttu-id="63cd2-105">Compressione sequenza</span><span class="sxs-lookup"><span data-stu-id="63cd2-105">Sequence Compression</span></span>

<span data-ttu-id="63cd2-106">L'applicazione può usare le funzioni [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)e [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) per comprimere una sequenza di frame.</span><span class="sxs-lookup"><span data-stu-id="63cd2-106">Your application can use the [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart), and [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) functions to compress a sequence of frames.</span></span> <span data-ttu-id="63cd2-107">Queste funzioni usano i dati archiviati nella struttura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) .</span><span class="sxs-lookup"><span data-stu-id="63cd2-107">These functions use the data stored in the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure.</span></span> <span data-ttu-id="63cd2-108">Le applicazioni usano la funzione [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) per consentire all'utente di selezionare un compressore, aprirlo e impostare i parametri di compressione nella struttura **COMPVARS** ; Tuttavia, le applicazioni possono impostare manualmente i parametri nella struttura.</span><span class="sxs-lookup"><span data-stu-id="63cd2-108">Applications use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to allow the user to select a compressor, open it, and set the compression parameters in the **COMPVARS** structure; however, applications can set the parameters in the structure manually.</span></span>

<span data-ttu-id="63cd2-109">Prima che un'applicazione possa iniziare a comprimere una sequenza di frame, deve usare **ICSeqCompressFrameStart** per allocare le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="63cd2-109">Before an application can begin compressing a sequence of frames, it must use **ICSeqCompressFrameStart** to allocate the necessary resources.</span></span> <span data-ttu-id="63cd2-110">Una volta allocate le risorse, l'applicazione può usare **ICSeqCompressFrame** per comprimere singolarmente ogni frame.</span><span class="sxs-lookup"><span data-stu-id="63cd2-110">After the resources are allocated, the application can use **ICSeqCompressFrame** to compress each frame individually.</span></span> <span data-ttu-id="63cd2-111">La frequenza dei fotogrammi e la frequenza del fotogramma chiave usati nella compressione della sequenza vengono specificati nei membri della struttura **COMPVARS** .</span><span class="sxs-lookup"><span data-stu-id="63cd2-111">The frame rate and key-frame frequency used in compressing the sequence are specified in members of the **COMPVARS** structure.</span></span> <span data-ttu-id="63cd2-112">Il valore restituito per **ICSeqCompressFrame** punta ai dati compressi.</span><span class="sxs-lookup"><span data-stu-id="63cd2-112">The return value for **ICSeqCompressFrame** points to the compressed data.</span></span>

<span data-ttu-id="63cd2-113">Quando un'applicazione termina la compressione di una sequenza, può usare **ICSeqCompressFrameEnd** per liberare le risorse di sistema allocate per **ICSeqCompressFrameStart**.</span><span class="sxs-lookup"><span data-stu-id="63cd2-113">When an application finishes compressing a sequence, it can use **ICSeqCompressFrameEnd** to free system resources allocated for **ICSeqCompressFrameStart**.</span></span> <span data-ttu-id="63cd2-114">Per liberare le risorse allocate per la struttura **COMPVARS** , l'applicazione può usare la funzione [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) .</span><span class="sxs-lookup"><span data-stu-id="63cd2-114">To free the resources allocated for the **COMPVARS** structure, the application can use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function.</span></span>

 

 




