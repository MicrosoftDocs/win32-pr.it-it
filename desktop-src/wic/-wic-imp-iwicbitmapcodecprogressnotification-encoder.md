---
description: Implementazione di IWICBitmapCodecProgressNotification (encoder)
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: Implementazione di IWICBitmapCodecProgressNotification (encoder)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883981"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a><span data-ttu-id="e4c2c-103">Implementazione di IWICBitmapCodecProgressNotification (encoder)</span><span class="sxs-lookup"><span data-stu-id="e4c2c-103">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="e4c2c-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="e4c2c-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="e4c2c-105">Sebbene l'interfaccia [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) sia facoltativa, è consigliabile implementarla nella classe del codificatore a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="e4c2c-105">Although the [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) interface is optional, it is recommended that it be implemented on the container-level encoder class.</span></span> <span data-ttu-id="e4c2c-106">Questa interfaccia viene illustrata in dettaglio nell' [implementazione di IWICBitmapCodecProgressNotification (decodificatore)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="e4c2c-106">This interface is discussed in more details in [Implementing IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span></span> <span data-ttu-id="e4c2c-107">L'implementazione è identica sia per il decodificatore che per il codificatore.</span><span class="sxs-lookup"><span data-stu-id="e4c2c-107">The implementation is the same for either the decoder and the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4c2c-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4c2c-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e4c2c-109">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e4c2c-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e4c2c-110">Implementazione di IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="e4c2c-110">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="e4c2c-111">Implementazione di IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="e4c2c-111">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="e4c2c-112">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="e4c2c-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="e4c2c-113">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="e4c2c-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="e4c2c-114">Implementazione di IWICBitmapCodecProgressNotification (decodificatore)</span><span class="sxs-lookup"><span data-stu-id="e4c2c-114">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



