---
description: Nella tabella seguente vengono descritti i thread sui quali è possibile attivare gli eventi degli oggetti RecognizerContext. EventThreadsRecognitionFires sul thread di riconoscimento in background o sul thread che chiama il metodo Recognize dell'oggetto RecognizerContext. RecognitionWithAlternatesFires nel thread di riconoscimento in background.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventi oggetto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968036"
---
# <a name="recognizercontext-object-events"></a><span data-ttu-id="61239-103">Eventi oggetto RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="61239-103">RecognizerContext Object Events</span></span>

<span data-ttu-id="61239-104">Nella tabella seguente vengono descritti i thread sui quali è possibile attivare gli eventi degli oggetti [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="61239-104">The following table describes which threads the [**RecognizerContext**](inkrecognizercontext-class.md) object events can fire on.</span></span>



| <span data-ttu-id="61239-105">Evento</span><span class="sxs-lookup"><span data-stu-id="61239-105">Event</span></span>                                                                               | <span data-ttu-id="61239-106">Thread</span><span class="sxs-lookup"><span data-stu-id="61239-106">Threads</span></span>                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61239-107">**Riconoscimento**</span><span class="sxs-lookup"><span data-stu-id="61239-107">**Recognition**</span></span>](inkrecognizercontext-recognition.md)                             | <span data-ttu-id="61239-108">Viene attivato sul thread di riconoscimento in background o sul thread che chiama il metodo [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="61239-108">Fires on the background recognition thread, or on the thread which calls the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method.</span></span><br/> |
| [<span data-ttu-id="61239-109">**RecognitionWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="61239-109">**RecognitionWithAlternates**</span></span>](inkrecognizercontext-recognitionwithalternates.md) | <span data-ttu-id="61239-110">Generato nel thread di riconoscimento in background.</span><span class="sxs-lookup"><span data-stu-id="61239-110">Fires on the background recognition thread.</span></span><br/>                                                                                                                                                               |



 

 

 




