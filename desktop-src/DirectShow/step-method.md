---
description: Il metodo Step sposta il flusso DVD-Video in base al numero di frame specificato.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Metodo Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316307"
---
# <a name="step-method"></a><span data-ttu-id="62d13-103">Metodo Step</span><span class="sxs-lookup"><span data-stu-id="62d13-103">Step Method</span></span>

> [!Note]  
> <span data-ttu-id="62d13-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="62d13-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="62d13-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="62d13-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="62d13-106">Il `Step` metodo fa avanzare il flusso DVD-Video in base al numero di frame specificato.</span><span class="sxs-lookup"><span data-stu-id="62d13-106">The `Step` method advances the DVD-Video stream by the specified number of frames.</span></span>

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a><span data-ttu-id="62d13-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="62d13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d13-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="62d13-108"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="62d13-109">Specifica il numero di frame da scorrere come Integer.</span><span class="sxs-lookup"><span data-stu-id="62d13-109">Specifies the number of frames to step as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62d13-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62d13-110">Return Value</span></span>

<span data-ttu-id="62d13-111">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="62d13-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62d13-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="62d13-112">Remarks</span></span>

<span data-ttu-id="62d13-113">Prima di chiamare questo metodo, chiamare [**CanStep**](canstep-method.md) per determinare se il decodificatore supporta l'esecuzione del frame.</span><span class="sxs-lookup"><span data-stu-id="62d13-113">Before calling this method, call [**CanStep**](canstep-method.md) to determine whether the decoder supports frame stepping.</span></span>

<span data-ttu-id="62d13-114">Se il DVD-Video viene riprodotto in modalità inversa quando viene chiamato questo metodo e il decodificatore supporta l'esecuzione di un frame inverso, l'esecuzione del frame viene eseguita in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="62d13-114">If the DVD-Video is playing in reverse mode when this method is called, and the decoder supports reverse frame stepping, then the frame stepping is done in reverse.</span></span>

 

 



