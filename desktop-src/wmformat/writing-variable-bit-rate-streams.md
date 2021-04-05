---
title: Scrittura di flussi di velocità in bit variabili
description: Scrittura di flussi di velocità in bit variabili
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Formato di sistemi avanzati (ASF), scrittura di flussi VBR
- ASF (Advanced Systems Format), scrittura di flussi VBR
- velocità in bit variabile (VBR), scrittura di flussi
- VBR (velocità in bit variabile), scrittura di flussi
- flussi, scrittura di VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723391"
---
# <a name="writing-variable-bit-rate-streams"></a><span data-ttu-id="1af25-108">Scrittura di flussi di velocità in bit variabili</span><span class="sxs-lookup"><span data-stu-id="1af25-108">Writing Variable Bit Rate Streams</span></span>

<span data-ttu-id="1af25-109">I flussi di velocità in bit variabile (VBR) vengono scritti allo stesso modo dei flussi di velocità in bit costante (CBR).</span><span class="sxs-lookup"><span data-stu-id="1af25-109">Variable bit rate (VBR) streams are written the same way as constant bit rate (CBR) streams.</span></span> <span data-ttu-id="1af25-110">L'unica differenza è rappresentata dall'elaborazione eseguita internamente dal writer e dai codec.</span><span class="sxs-lookup"><span data-stu-id="1af25-110">The only difference is in the processing performed internally by the writer and the codecs.</span></span> <span data-ttu-id="1af25-111">Tuttavia, la velocità in bit basata su VBR (sia vincolata che non vincolata) richiede un passaggio di pre-elaborazione nel writer.</span><span class="sxs-lookup"><span data-stu-id="1af25-111">However, bit rate based VBR (both constrained and unconstrained) requires a preprocessing pass in the writer.</span></span>

<span data-ttu-id="1af25-112">È necessario controllare il valore restituito per la prima chiamata a [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="1af25-112">You should check the return value for the first call you make to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) for each stream.</span></span> <span data-ttu-id="1af25-113">Se il codice di errore restituito è NS E il numero di \_ \_ passaggi non è valido \_ \_ , il flusso richiede un passaggio di pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="1af25-113">If the error code returned is NS\_E\_INVALID\_NUM\_PASSES, the stream requires a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1af25-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1af25-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1af25-115">**Uso della codifica Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="1af25-115">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="1af25-116">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="1af25-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




