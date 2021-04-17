---
description: Specifica il livello di normalizzazione della finestra di dialogo, in decibel (dB), in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Proprietà AVEncDDDialogNormalization (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 586f241dc8d032767ecb2678c1ee5704dc20e0ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482493"
---
# <a name="avencdddialognormalization-property"></a><span data-ttu-id="a96c7-104">Proprietà AVEncDDDialogNormalization</span><span class="sxs-lookup"><span data-stu-id="a96c7-104">AVEncDDDialogNormalization property</span></span>

<span data-ttu-id="a96c7-105">Specifica il livello di normalizzazione della finestra di dialogo, in decibel (dB), in un flusso audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="a96c7-105">Specifies the dialog normalization level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="a96c7-106">Questa proprietà si applica ai codificatori audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="a96c7-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="a96c7-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a96c7-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a96c7-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a96c7-108">Data type</span></span>

<span data-ttu-id="a96c7-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a96c7-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a96c7-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="a96c7-110">Property GUID</span></span>

<span data-ttu-id="a96c7-111">**Codecapis \_ AVEncDDDialogNormalization**</span><span class="sxs-lookup"><span data-stu-id="a96c7-111">**CODECAPI\_AVEncDDDialogNormalization**</span></span>

## <a name="property-value"></a><span data-ttu-id="a96c7-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a96c7-112">Property value</span></span>

<span data-ttu-id="a96c7-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="a96c7-113">This property has a linear range of values.</span></span> <span data-ttu-id="a96c7-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="a96c7-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="a96c7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a96c7-115">Requirements</span></span>



| <span data-ttu-id="a96c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a96c7-116">Requirement</span></span> | <span data-ttu-id="a96c7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a96c7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a96c7-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a96c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a96c7-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a96c7-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a96c7-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a96c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a96c7-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a96c7-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a96c7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a96c7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a96c7-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a96c7-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a96c7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a96c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a96c7-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="a96c7-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a96c7-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a96c7-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




