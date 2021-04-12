---
description: La proprietà volume imposta o Recupera il volume del altoparlante per l'output del flusso audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Proprietà Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527805"
---
# <a name="volume-property"></a><span data-ttu-id="82654-103">Proprietà Volume</span><span class="sxs-lookup"><span data-stu-id="82654-103">Volume Property</span></span>

> [!Note]  
> <span data-ttu-id="82654-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="82654-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="82654-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="82654-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="82654-106">La `Volume` proprietà imposta o Recupera il volume del altoparlante per l'output del flusso audio.</span><span class="sxs-lookup"><span data-stu-id="82654-106">The `Volume` property sets or retrieves the speaker volume for the audio stream output.</span></span>

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a><span data-ttu-id="82654-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82654-107">Return Value</span></span>

<span data-ttu-id="82654-108">Restituisce il livello del volume come attenuazione in decibel come valore integer.</span><span class="sxs-lookup"><span data-stu-id="82654-108">Returns the volume level as attenuation in decibels as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="82654-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="82654-109">Remarks</span></span>

<span data-ttu-id="82654-110">Questa proprietà è di lettura/scrittura e il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="82654-110">This property is read/write with a default value of 0.</span></span> <span data-ttu-id="82654-111">Il volume completo è 0 e 10.000 è silenzioso; la scala è logaritmica.</span><span class="sxs-lookup"><span data-stu-id="82654-111">Full volume is 0, and 10,000 is silence; the scale is logarithmic.</span></span> <span data-ttu-id="82654-112">Moltiplicare il livello di decibel desiderato di 100 (ad esempio, 10.000 = 100 dB).</span><span class="sxs-lookup"><span data-stu-id="82654-112">Multiply the desired decibel level by 100 (for example 10,000 = 100 dB).</span></span>

 

 



