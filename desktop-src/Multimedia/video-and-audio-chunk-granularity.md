---
title: Granularità dei blocchi video e audio
description: Granularità dei blocchi video e audio
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- File AVI, granularità dei blocchi
- Classe AVICap, blocchi filler
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955585"
---
# <a name="video-and-audio-chunk-granularity"></a><span data-ttu-id="56023-109">Granularità dei blocchi video e audio</span><span class="sxs-lookup"><span data-stu-id="56023-109">Video and Audio Chunk Granularity</span></span>

<span data-ttu-id="56023-110">La granularità del blocco è una dimensione del blocco logico per un file AVI usato per la scrittura e il recupero di blocchi di dati audio e video.</span><span class="sxs-lookup"><span data-stu-id="56023-110">The chunk granularity is a logical block size for an AVI file that is used for writing and retrieving audio and video data chunks.</span></span> <span data-ttu-id="56023-111">Quando si scrivono blocchi audio e video su disco, AVICap aggiunge blocchi di riempimento (blocchi "spazzatura") necessari per riempire ogni blocco logico di dati.</span><span class="sxs-lookup"><span data-stu-id="56023-111">When writing audio and video chunks to disk, AVICap adds filler chunks (RIFF "JUNK" chunks) as necessary to fill each logical block of data.</span></span>

<span data-ttu-id="56023-112">È possibile recuperare l'impostazione di granularità del blocco corrente usando il messaggio di [**installazione della sequenza di WM \_ Cap \_ \_ \_ Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="56023-112">You can retrieve the current chunk granularity setting by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="56023-113">La granularità del blocco corrente viene archiviata nel membro **wChunkGranularity** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="56023-113">The current chunk granularity is stored in the **wChunkGranularity** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="56023-114">È possibile specificare una nuova granularità dei blocchi come valore di **wChunkGranularity** , quindi inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ di set di WM Cap**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="56023-114">You can specify a new chunk granularity as the value of **wChunkGranularity** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="56023-115">È anche possibile specificare zero per questo membro per impostare la granularità dei blocchi sulle dimensioni del settore del disco.</span><span class="sxs-lookup"><span data-stu-id="56023-115">You can also specify zero for this member to set the chunk granularity to the sector size of the disk.</span></span>

 

 




