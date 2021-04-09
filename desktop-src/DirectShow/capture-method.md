---
description: Il metodo Capture acquisisce un'immagine ancora dal fotogramma video quando l'oggetto MSWebDVD è in modalità senza finestra.
ms.assetid: 704e64ef-3593-403c-8ecf-625fb4983882
title: Metodo Capture
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db16bbc6ef50de303dbcdac66bd066861bb5811
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123642"
---
# <a name="capture-method"></a><span data-ttu-id="5b82a-103">Metodo Capture</span><span class="sxs-lookup"><span data-stu-id="5b82a-103">Capture Method</span></span>

> [!Note]  
> <span data-ttu-id="5b82a-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5b82a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5b82a-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="5b82a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5b82a-106">Il `Capture` metodo acquisisce un'immagine ancora dal fotogramma video quando l'oggetto mswebdvd è in modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="5b82a-106">The `Capture` method captures a still image from the video frame when the MSWebDVD object is in windowless mode.</span></span>

``` syntax
MSWebDVD.Capture()
```

## <a name="remarks"></a><span data-ttu-id="5b82a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b82a-107">Remarks</span></span>

<span data-ttu-id="5b82a-108">Questo metodo acquisisce il frame corrente dall'immagine DVD-Video e lo incolla in una finestra da cui l'utente può salvare o modificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="5b82a-108">This method captures the current frame from the DVD-Video image and pastes it into a window from which the user can save or edit the image.</span></span> <span data-ttu-id="5b82a-109">L'oggetto MSWebDVD deve essere in modalità senza finestra affinché questo metodo abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5b82a-109">The MSWebDVD object must be in windowless mode for this method to succeed.</span></span>

 

 



