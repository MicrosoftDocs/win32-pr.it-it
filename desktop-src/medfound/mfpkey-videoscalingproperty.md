---
description: Specifica se il codec utilizzerà l'ottimizzazione del ridimensionamento del video.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: Proprietà MFPKEY_VIDEOSCALING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880626"
---
# <a name="mfpkey_videoscaling-property"></a><span data-ttu-id="9ccc4-103">\_Proprietà VIDEOSCALING di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="9ccc4-103">MFPKEY\_VIDEOSCALING Property</span></span>

<span data-ttu-id="9ccc4-104">Specifica se il codec utilizzerà l'ottimizzazione del ridimensionamento del video.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-104">Specifies whether the codec will use video scaling optimization.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9ccc4-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9ccc4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9ccc4-106">g \_ wszWMVCVideoScaling</span><span class="sxs-lookup"><span data-stu-id="9ccc4-106">g\_wszWMVCVideoScaling</span></span>

## <a name="data-type"></a><span data-ttu-id="9ccc4-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9ccc4-107">Data Type</span></span>

<span data-ttu-id="9ccc4-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9ccc4-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="9ccc4-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="9ccc4-109">Default Value</span></span>

<span data-ttu-id="9ccc4-110">0</span><span class="sxs-lookup"><span data-stu-id="9ccc4-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="9ccc4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ccc4-111">Remarks</span></span>

<span data-ttu-id="9ccc4-112">Il ridimensionamento video è un tipo di ottimizzazione percettiva che può migliorare la qualità visiva del video codificato a velocità in bit basso.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-112">Video scaling is a type of perceptual optimization that can improve the visual quality of video encoded at low bit rates.</span></span> <span data-ttu-id="9ccc4-113">L'ottimizzazione del ridimensionamento del video riduce gli artefatti pronunciati, ma può sacrificare i dettagli dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-113">The video scaling optimization reduces pronounced artifacts, but can sacrifice image detail.</span></span> <span data-ttu-id="9ccc4-114">Questa ottimizzazione influisce sull'intervallo di Luma del video codificato, come descritto di seguito, ma non influisce sulla risoluzione fisica del video di output.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-114">This optimization affects the luma range of the encoded video as described below but does not affect the physical resolution of the output video.</span></span>

<span data-ttu-id="9ccc4-115">Questa proprietà può essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-115">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="9ccc4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9ccc4-116">Value</span></span> | <span data-ttu-id="9ccc4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ccc4-117">Description</span></span>                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccc4-118">0</span><span class="sxs-lookup"><span data-stu-id="9ccc4-118">0</span></span>     | <span data-ttu-id="9ccc4-119">Il ridimensionamento video non verrà usato.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-119">Video scaling will not be used.</span></span>                                                                                       |
| <span data-ttu-id="9ccc4-120">1</span><span class="sxs-lookup"><span data-stu-id="9ccc4-120">1</span></span>     | <span data-ttu-id="9ccc4-121">Il codificatore userà l'ottimizzazione del ridimensionamento video conservativa.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-121">The encoder will use conservative video scaling optimization.</span></span> <span data-ttu-id="9ccc4-122">L'intervallo di Luma verrà ridimensionato da 0... 255 a 26... 229.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-122">The luma range will be scaled from 0...255 to 26...229.</span></span> |
| <span data-ttu-id="9ccc4-123">2</span><span class="sxs-lookup"><span data-stu-id="9ccc4-123">2</span></span>     | <span data-ttu-id="9ccc4-124">Il codificatore userà un'ottimizzazione di ridimensionamento video aggressiva.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-124">The encoder will use aggressive video scaling optimization.</span></span> <span data-ttu-id="9ccc4-125">L'intervallo di Luma verrà ridimensionato da 0... 255 a 31... 224.</span><span class="sxs-lookup"><span data-stu-id="9ccc4-125">The luma range will be scaled from 0...255 to 31...224.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="9ccc4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ccc4-126">Requirements</span></span>



| <span data-ttu-id="9ccc4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ccc4-127">Requirement</span></span> | <span data-ttu-id="9ccc4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9ccc4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccc4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ccc4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9ccc4-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ccc4-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ccc4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ccc4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9ccc4-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ccc4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ccc4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ccc4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ccc4-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ccc4-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ccc4-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ccc4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ccc4-136">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9ccc4-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




