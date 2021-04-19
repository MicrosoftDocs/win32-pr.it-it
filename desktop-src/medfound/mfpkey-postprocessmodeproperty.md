---
description: Specifica la modalità di post-elaborazione per il decodificatore.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: Proprietà MFPKEY_POSTPROCESSMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333092"
---
# <a name="mfpkey_postprocessmode-property"></a><span data-ttu-id="42e54-103">\_Proprietà POSTPROCESSMODE di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="42e54-103">MFPKEY\_POSTPROCESSMODE Property</span></span>

<span data-ttu-id="42e54-104">Specifica la modalità di post-elaborazione per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="42e54-104">Specifies the post processing mode for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="42e54-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="42e54-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="42e54-106">**g \_ wszWMVCForcePostProcessMode**</span><span class="sxs-lookup"><span data-stu-id="42e54-106">**g\_wszWMVCForcePostProcessMode**</span></span>

## <a name="data-type"></a><span data-ttu-id="42e54-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="42e54-107">Data Type</span></span>

<span data-ttu-id="42e54-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="42e54-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="42e54-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="42e54-109">Remarks</span></span>

<span data-ttu-id="42e54-110">Impostare questa proprietà su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="42e54-110">Set this property to one of the following values.</span></span>



| <span data-ttu-id="42e54-111">Valore</span><span class="sxs-lookup"><span data-stu-id="42e54-111">Value</span></span> | <span data-ttu-id="42e54-112">Significato</span><span class="sxs-lookup"><span data-stu-id="42e54-112">Meaning</span></span>                                                                                |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42e54-113">-1</span><span class="sxs-lookup"><span data-stu-id="42e54-113">-1</span></span>    | <span data-ttu-id="42e54-114">Il decodificatore imposta la modalità di post-elaborazione in modo adattivo in base alle risorse della CPU disponibili.</span><span class="sxs-lookup"><span data-stu-id="42e54-114">The decoder sets the post processing mode adaptively based on available CPU resources.</span></span> |
| <span data-ttu-id="42e54-115">0</span><span class="sxs-lookup"><span data-stu-id="42e54-115">0</span></span>     | <span data-ttu-id="42e54-116">Il decodificatore non esegue alcuna post-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="42e54-116">The decoder performs no post processing.</span></span>                                               |
| <span data-ttu-id="42e54-117">1</span><span class="sxs-lookup"><span data-stu-id="42e54-117">1</span></span>     | <span data-ttu-id="42e54-118">il decodificatore della esegue un deblocco rapido.</span><span class="sxs-lookup"><span data-stu-id="42e54-118">fThe decoder performs fast deblocking.</span></span>                                                 |
| <span data-ttu-id="42e54-119">2</span><span class="sxs-lookup"><span data-stu-id="42e54-119">2</span></span>     | <span data-ttu-id="42e54-120">Il decodificatore esegue il deblocco completo.</span><span class="sxs-lookup"><span data-stu-id="42e54-120">The decoder performs full deblocking.</span></span>                                                  |
| <span data-ttu-id="42e54-121">3</span><span class="sxs-lookup"><span data-stu-id="42e54-121">3</span></span>     | <span data-ttu-id="42e54-122">Il decodificatore esegue una rapida deblocco e una chiamata.</span><span class="sxs-lookup"><span data-stu-id="42e54-122">The decoder performs fast deblocking and deringing.</span></span>                                    |
| <span data-ttu-id="42e54-123">4</span><span class="sxs-lookup"><span data-stu-id="42e54-123">4</span></span>     | <span data-ttu-id="42e54-124">Il decodificatore esegue il blocco e la dechiamata completi.</span><span class="sxs-lookup"><span data-stu-id="42e54-124">The decoder performs full deblocking and deringing.</span></span>                                    |



 

<span data-ttu-id="42e54-125">Poiché il valore di questa proprietà va da 0 a 4, la complessità di decodifica, l'utilizzo delle risorse della CPU e la qualità dell'immagine aumentano.</span><span class="sxs-lookup"><span data-stu-id="42e54-125">As the value of this property goes from 0 to 4, the decoding complexity, use of CPU resources, and picture quality all increase.</span></span>

## <a name="requirements"></a><span data-ttu-id="42e54-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42e54-126">Requirements</span></span>



| <span data-ttu-id="42e54-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="42e54-127">Requirement</span></span> | <span data-ttu-id="42e54-128">Valore</span><span class="sxs-lookup"><span data-stu-id="42e54-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42e54-129">Client</span><span class="sxs-lookup"><span data-stu-id="42e54-129">Client</span></span><br/> | <span data-ttu-id="42e54-130">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="42e54-130">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="42e54-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42e54-131">Header</span></span><br/> | <dl> <span data-ttu-id="42e54-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42e54-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e54-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42e54-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e54-134">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42e54-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




