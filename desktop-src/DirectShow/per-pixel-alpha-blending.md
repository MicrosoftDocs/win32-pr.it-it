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
# <a name="per-pixel-alpha-blending"></a>Per-Pixel la fusione alfa

Sono stati definiti quattro sottotipi di supporti per la fusione alfa per pixel. Questi sottotipi sono supportati solo quando VMR è in modalità di combinazione. Il VMR rifiuterà la connessione se non si trova in modalità di combinazione quando un filtro upstream tenta di connettersi usando uno di questi sottotipi. Questi sottotipi sono definiti in UUIDs. h:

-   \_ARGB1555 MEDIASUBTYPE
-   \_ARGB4444 MEDIASUBTYPE
-   \_ARGB32 MEDIASUBTYPE
-   \_AYUV MEDIASUBTYPE

Per altre informazioni, vedere [sottotipi video RGB non compressi](uncompressed-rgb-video-subtypes.md) e [**sottotipi video YUV**](yuv-video-subtypes.md).

 

 



