---
description: Per-Pixel la fusione alfa
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel la fusione alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303986"
---
# <a name="per-pixel-alpha-blending"></a><span data-ttu-id="a6975-103">Per-Pixel la fusione alfa</span><span class="sxs-lookup"><span data-stu-id="a6975-103">Per-Pixel Alpha Blending</span></span>

<span data-ttu-id="a6975-104">Sono stati definiti quattro sottotipi di supporti per la fusione alfa per pixel.</span><span class="sxs-lookup"><span data-stu-id="a6975-104">Four media subtypes have been defined for per-pixel alpha blending.</span></span> <span data-ttu-id="a6975-105">Questi sottotipi sono supportati solo quando VMR è in modalità di combinazione.</span><span class="sxs-lookup"><span data-stu-id="a6975-105">These subtypes are only supported when the VMR is in mixing mode.</span></span> <span data-ttu-id="a6975-106">Il VMR rifiuterà la connessione se non si trova in modalità di combinazione quando un filtro upstream tenta di connettersi usando uno di questi sottotipi.</span><span class="sxs-lookup"><span data-stu-id="a6975-106">The VMR will reject the connection if it is not in mixing mode when an upstream filter attempts to connect using one of these subtypes.</span></span> <span data-ttu-id="a6975-107">Questi sottotipi sono definiti in UUIDs. h:</span><span class="sxs-lookup"><span data-stu-id="a6975-107">These subtypes are defined in uuids.h:</span></span>

-   <span data-ttu-id="a6975-108">\_ARGB1555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="a6975-108">MEDIASUBTYPE\_ARGB1555</span></span>
-   <span data-ttu-id="a6975-109">\_ARGB4444 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="a6975-109">MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="a6975-110">\_ARGB32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="a6975-110">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="a6975-111">\_AYUV MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="a6975-111">MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="a6975-112">Per altre informazioni, vedere [sottotipi video RGB non compressi](uncompressed-rgb-video-subtypes.md) e [**sottotipi video YUV**](yuv-video-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="a6975-112">For more information, see [Uncompressed RGB Video Subtypes](uncompressed-rgb-video-subtypes.md) and [**YUV Video Subtypes**](yuv-video-subtypes.md).</span></span>

 

 



