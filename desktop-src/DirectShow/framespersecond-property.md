---
description: La proprietà FramesPerSecond recupera la frequenza dei fotogrammi video per il titolo del DVD corrente.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Proprietà FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303966"
---
# <a name="framespersecond-property"></a><span data-ttu-id="b1926-103">Proprietà FramesPerSecond</span><span class="sxs-lookup"><span data-stu-id="b1926-103">FramesPerSecond Property</span></span>

> [!Note]  
> <span data-ttu-id="b1926-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b1926-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b1926-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b1926-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b1926-106">La `FramesPerSecond` proprietà recupera la frequenza dei fotogrammi video per il titolo del DVD corrente.</span><span class="sxs-lookup"><span data-stu-id="b1926-106">The `FramesPerSecond` property retrieves the video frame rate for the current DVD title.</span></span>

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a><span data-ttu-id="b1926-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1926-107">Return Value</span></span>

<span data-ttu-id="b1926-108">Restituisce un valore intero che rappresenta la frequenza dei fotogrammi video; 25 o 30 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="b1926-108">Returns an integer value representing the video frame rate; either 25 or 30 frames per second.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1926-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1926-109">Remarks</span></span>

<span data-ttu-id="b1926-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b1926-110">This property is read-only with no default value.</span></span> <span data-ttu-id="b1926-111">I segnali video NTSC vengono visualizzati a 30 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="b1926-111">NTSC video signals are displayed at 30 frames per second.</span></span> <span data-ttu-id="b1926-112">PAL viene visualizzato a 25 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="b1926-112">PAL is displayed at 25 frames per second.</span></span> <span data-ttu-id="b1926-113">Un disco è codificato per la riproduzione in NTSC o PAL, ma non può essere riprodotto in entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="b1926-113">A disc is encoded to play on either NTSC or PAL, but cannot play on both.</span></span>

 

 



