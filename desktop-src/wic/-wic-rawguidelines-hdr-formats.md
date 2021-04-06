---
description: Formati pixel con intervallo dinamico elevato
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formati pixel con intervallo dinamico elevato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883966"
---
# <a name="high-dynamic-range-pixel-formats"></a><span data-ttu-id="687d9-103">Formati pixel con intervallo dinamico elevato</span><span class="sxs-lookup"><span data-stu-id="687d9-103">High Dynamic Range Pixel Formats</span></span>

<span data-ttu-id="687d9-104">I codec devono usare formati pixel di Windows Imaging Component (WIC) che conservano tutti gli intervalli dinamici dei dati dei sensori sottostanti.</span><span class="sxs-lookup"><span data-stu-id="687d9-104">Codecs should use Windows Imaging Component (WIC) pixel formats that preserve all of the dynamic range of the underlying sensor data.</span></span> <span data-ttu-id="687d9-105">GUID \_ WICPixelFormat48bppRGB è un tipico formato a virgola fissa a 16 bit per canale che può essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="687d9-105">GUID\_WICPixelFormat48bppRGB is a typical fixed-point 16-bit-per-channel format that can be used.</span></span> <span data-ttu-id="687d9-106">È anche possibile usare altri formati con precisione più elevata.</span><span class="sxs-lookup"><span data-stu-id="687d9-106">Other higher precision formats can be used also.</span></span> <span data-ttu-id="687d9-107">Per abilitare il supporto completo per la pipeline di rendering con accelerazione della Windows Presentation Foundation GPU (Graphics Processing Unit), Microsoft consiglia vivamente di supportare un formato pixel a virgola mobile a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="687d9-107">To enable full support for the Windows Presentation Foundation graphics processing unit (GPU)-accelerated rendering pipeline, Microsoft strongly encourages support for a 32-bit floating point pixel format.</span></span>

<span data-ttu-id="687d9-108">Formati pixel di colore elevato: con Windows 7 sono stati aggiunti due nuovi formati pixel WIC per supportare i nuovi formati di visualizzazione a colori elevati.</span><span class="sxs-lookup"><span data-stu-id="687d9-108">High Color Pixel Formats: With Windows 7, two new WIC pixel formats have been added to support the new High Color display formats.</span></span> <span data-ttu-id="687d9-109">Ovvero GUID \_ WICPixelFormat32bppRGBA1010102 e GUID \_ WICPixelFormat32bppRGBA1010102XR.</span><span class="sxs-lookup"><span data-stu-id="687d9-109">These are: GUID\_WICPixelFormat32bppRGBA1010102 and GUID\_WICPixelFormat32bppRGBA1010102XR.</span></span>

<span data-ttu-id="687d9-110">Il formato a colori elevato float a 16 bit per canale (bpc) è supportato dal \_ formato pixel WICPIXELFORMAT64BPPRGBAHALF GUID esistente.</span><span class="sxs-lookup"><span data-stu-id="687d9-110">The 16 bit per channel (bpc) float High Color format is supported by the existing GUID\_WICPixelFormat64bppRGBAHalf pixel format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="687d9-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="687d9-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="687d9-112">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="687d9-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="687d9-113">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="687d9-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="687d9-114">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="687d9-114">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="687d9-115">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="687d9-115">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



