---
description: Il metodo GetVideoSize recupera le dimensioni video native.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Metodo GetVideoSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304386"
---
# <a name="getvideosize-method"></a><span data-ttu-id="bebd1-103">Metodo GetVideoSize</span><span class="sxs-lookup"><span data-stu-id="bebd1-103">GetVideoSize Method</span></span>

> [!Note]  
> <span data-ttu-id="bebd1-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bebd1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bebd1-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="bebd1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bebd1-106">Il `GetVideoSize` metodo recupera le dimensioni video native.</span><span class="sxs-lookup"><span data-stu-id="bebd1-106">The `GetVideoSize` method retrieves the native video dimensions.</span></span>

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a><span data-ttu-id="bebd1-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bebd1-107">Return Value</span></span>

<span data-ttu-id="bebd1-108">Restituisce un oggetto [DVDRect](dvdrect-object.md) che contiene quattro proprietà di lettura/scrittura: (in alto a sinistra) x; (in alto a sinistra) y, larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="bebd1-108">Returns a [DVDRect](dvdrect-object.md) object containing four read/write properties: (top left) x; (top left) y, Width, and Height.</span></span> <span data-ttu-id="bebd1-109">Le proprietà **x** e **y** sono impostate su zero e le altre due proprietà riflettono la larghezza e l'altezza del rettangolo video come creato sul disco.</span><span class="sxs-lookup"><span data-stu-id="bebd1-109">The **x** and **y** properties are set to zero and the other two properties reflect the width and height of the video rectangle as authored on the disc.</span></span>

 

 



