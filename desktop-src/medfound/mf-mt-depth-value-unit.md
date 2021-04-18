---
description: Valore che definisce le unità per un valore di profondità in un frame video.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: Attributo MF_MT_DEPTH_VALUE_UNIT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309549"
---
# <a name="mf_mt_depth_value_unit-attribute"></a><span data-ttu-id="adc35-103">\_ \_ \_ Attributo unità valore di profondità MF mt \_</span><span class="sxs-lookup"><span data-stu-id="adc35-103">MF\_MT\_DEPTH\_VALUE\_UNIT attribute</span></span>

<span data-ttu-id="adc35-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="adc35-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="adc35-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="adc35-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="adc35-106">Valore che definisce le unità per un valore di profondità in un frame video.</span><span class="sxs-lookup"><span data-stu-id="adc35-106">A value that defines the units for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="adc35-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="adc35-107">Data type</span></span>

<span data-ttu-id="adc35-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="adc35-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="adc35-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="adc35-109">Remarks</span></span>

<span data-ttu-id="adc35-110">Il valore dell'unità è un valore UINT64 in nanometri, compreso tra 1e-9 contatori.</span><span class="sxs-lookup"><span data-stu-id="adc35-110">The unit value is a UINT64 value in nanometers, in the range 1e - 9 meters.</span></span> <span data-ttu-id="adc35-111">Se questo valore non è presente, il valore predefinito dell'unità è 1e-3, che indica che ogni livello di pixel viene misurato in 1 mm nello spazio fisico.</span><span class="sxs-lookup"><span data-stu-id="adc35-111">If this value is not present, the default value of the unit is 1e-3, which indicates each pixel level is measured in 1 millimeter in physical space.</span></span>

<span data-ttu-id="adc35-112">Le fotocamere con profondità non possono comprendere la profondità di tutti i pixel.</span><span class="sxs-lookup"><span data-stu-id="adc35-112">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="adc35-113">Quando la confidenza di un pixel è bassa, a causa di materiale, occlusione o non compreso nell'intervallo e così via, il valore di profondità su tale pixel può non essere valido.</span><span class="sxs-lookup"><span data-stu-id="adc35-113">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="adc35-114">Quando un valore di pixel di profondità è 0, il pixel non è valido.</span><span class="sxs-lookup"><span data-stu-id="adc35-114">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="adc35-115">Alcune fotocamere di profondità allineano i metadati della maschera di maschera per ogni pixel oltre al valore di profondità per rappresentare il motivo per cui la profondità del pixel non è valida, a causa del materiale, dell'occlusione o dell'intervallo e così via. Si consiglia di evitare di alleghiare tali metadati come valori di profondità, perché in genere si verificano difficoltà quando si utilizzano tali valori in pixel shader.</span><span class="sxs-lookup"><span data-stu-id="adc35-115">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="adc35-116">Invece.</span><span class="sxs-lookup"><span data-stu-id="adc35-116">Instead.</span></span> <span data-ttu-id="adc35-117">si consiglia di usare un buffer di immagini a 8 bit separato con la stessa risoluzione e di associarlo come attributo di [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="adc35-117">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="adc35-118">Tali metadati variano a seconda del fornitore della fotocamera e non sono standardizzati dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="adc35-118">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="adc35-119">È consigliabile usare 16 bit completi per il valore di profondità per semplificare l'elaborazione a valle e usare un valore fisso, ad esempio 0, per l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="adc35-119">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="adc35-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="adc35-120">Requirements</span></span>



| <span data-ttu-id="adc35-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="adc35-121">Requirement</span></span> | <span data-ttu-id="adc35-122">Valore</span><span class="sxs-lookup"><span data-stu-id="adc35-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="adc35-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adc35-123">Minimum supported client</span></span><br/> | <span data-ttu-id="adc35-124">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="adc35-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="adc35-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adc35-125">Minimum supported server</span></span><br/> | <span data-ttu-id="adc35-126">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="adc35-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="adc35-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="adc35-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="adc35-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="adc35-128"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




