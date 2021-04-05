---
title: Proprietà MinimumScaleRotateRadius di IManipulationProcessor
description: Specifica la dimensione dei contatti di distanza in un movimento di ridimensionamento o rotazione che devono essere per attivare la manipolazione.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Proprietà di MinimumScaleRotateRadius Windows Touch
- Proprietà MinimumScaleRotateRadius Windows Touch, interfaccia IManipulationProcessor
- Interfaccia IManipulationProcessor Windows Touch, Proprietà MinimumScaleRotateRadius
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718619"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a><span data-ttu-id="c6411-106">Proprietà IManipulationProcessor:: MinimumScaleRotateRadius</span><span class="sxs-lookup"><span data-stu-id="c6411-106">IManipulationProcessor::MinimumScaleRotateRadius property</span></span>

<span data-ttu-id="c6411-107">Specifica la dimensione dei contatti di distanza in un movimento di ridimensionamento o rotazione che devono essere per attivare la manipolazione.</span><span class="sxs-lookup"><span data-stu-id="c6411-107">Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.</span></span>

<span data-ttu-id="c6411-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6411-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6411-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6411-109">Syntax</span></span>


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a><span data-ttu-id="c6411-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c6411-110">Property value</span></span>

<span data-ttu-id="c6411-111">Specifica la distanza minima tra i contatti per attivare il ridimensionamento o la rotazione dei movimenti.</span><span class="sxs-lookup"><span data-stu-id="c6411-111">Specifies the minimum distance between contacts to trigger scale or rotate gestures.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c6411-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c6411-112">Error codes</span></span>

## <a name="remarks"></a><span data-ttu-id="c6411-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6411-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c6411-114">Questa proprietà viene impostata in centipixels (100 di un pixel).</span><span class="sxs-lookup"><span data-stu-id="c6411-114">This property is set in centipixels (100ths of a pixel).</span></span>

 

<span data-ttu-id="c6411-115">Impostando questo valore si farà in modo che il processore di manipolazione ignori i movimenti con un raggio troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="c6411-115">Setting this value will make the manipulation processor ignore gestures that have too small of a radius.</span></span> <span data-ttu-id="c6411-116">Questa opzione è utile se si desidera impedire a un utente di modificare un oggetto in un raggio troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="c6411-116">This is useful if you want to prevent a user from manipulating an object to too small of a radius.</span></span> <span data-ttu-id="c6411-117">Se, ad esempio, si utilizza un processore di manipolazione con un cerchio e si desidera assicurarsi che mantenga un raggio maggiore di 100 pixel, impostare questo valore su 10000.</span><span class="sxs-lookup"><span data-stu-id="c6411-117">For example, if you are using a manipulation processor with a circle and want the ensure that it maintains a radius greater than 100 pixels, you would set this value to 10000.</span></span>

## <a name="examples"></a><span data-ttu-id="c6411-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="c6411-118">Examples</span></span>


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a><span data-ttu-id="c6411-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c6411-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6411-120">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="c6411-120">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




