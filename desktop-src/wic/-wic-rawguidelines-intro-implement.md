---
description: Linee guida generali per l'implementazione di codec non ELABORAti
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Linee guida generali per l'implementazione di codec non ELABORAti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232878"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a><span data-ttu-id="883c2-103">Linee guida generali per l'implementazione di codec non ELABORAti</span><span class="sxs-lookup"><span data-stu-id="883c2-103">General Guidelines for Implementing RAW Codecs</span></span>

<span data-ttu-id="883c2-104">Rispetto ai tipi di immagine non ELABORAti, ad esempio JPEG o TIFF, esistono due differenze significative nel modo in cui si prevede che i formati di immagine RAW si comportino in Windows:</span><span class="sxs-lookup"><span data-stu-id="883c2-104">Compared to non-RAW image types such as JPEG or TIFF, there are two notable differences in how RAW image formats are expected to behave in Windows:</span></span>

-   <span data-ttu-id="883c2-105">La maggior parte dei formati di immagine non ELABORAta si presume essere di sola lettura e probabilmente non supporterà la codifica pixel in formato non elaborato.</span><span class="sxs-lookup"><span data-stu-id="883c2-105">Most RAW image formats are presumed to be "read only" and probably will not support pixel encoding to RAW format.</span></span> <span data-ttu-id="883c2-106">Tuttavia, poiché Windows Imaging Component (WIC) richiede che un codificatore supporti il writeback dei metadati, gli autori di codec non ELABORAti devono pianificare l'implementazione di almeno una classe Skeleton Encoder.</span><span class="sxs-lookup"><span data-stu-id="883c2-106">However, because Windows Imaging Component (WIC) requires an encoder to support metadata write-back, RAW codec authors should plan to implement at least a skeleton encoder class.</span></span>
-   <span data-ttu-id="883c2-107">La decodifica di un'immagine RAW a dimensione intera può richiedere molto tempo rispetto ad altri formati.</span><span class="sxs-lookup"><span data-stu-id="883c2-107">Decoding a full-size RAW image can take a long time compared to other formats.</span></span> <span data-ttu-id="883c2-108">Per questo motivo, Microsoft consiglia di adottare determinati approcci per ridurre al minimo la latenza di decodifica e per garantire il supporto per scenari come il rendering rapido di anteprime e anteprime.</span><span class="sxs-lookup"><span data-stu-id="883c2-108">For this reason, Microsoft recommends that certain approaches be taken to minimize decoding latency and to ensure support for scenarios such as rapid rendering of thumbnails and previews.</span></span>

    <span data-ttu-id="883c2-109">Tutti gli autori di codec RAW, ad esempio, devono implementare l'interfaccia [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , che fornisce un meccanismo per inviare una notifica al decodificatore in anticipo rispetto alla dimensione bitmap di destinazione, consentendo così la decodifica ottimizzata a una dimensione dell'immagine di output inferiore.</span><span class="sxs-lookup"><span data-stu-id="883c2-109">For example, all RAW codec authors must implement the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface, which provides a mechanism to notify the decoder in advance of the target bitmap size, thus enabling optimized decoding to a smaller output image size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="883c2-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="883c2-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="883c2-111">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="883c2-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="883c2-112">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="883c2-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="883c2-113">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="883c2-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="883c2-114">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="883c2-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



