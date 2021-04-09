---
description: Specifica il numero predefinito di fotogrammi B consecutivi tra I frame I e P.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Proprietà AVEncMPVDefaultBPictureCount (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049025"
---
# <a name="avencmpvdefaultbpicturecount-property"></a><span data-ttu-id="aee02-103">Proprietà AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="aee02-103">AVEncMPVDefaultBPictureCount property</span></span>

<span data-ttu-id="aee02-104">Specifica il numero predefinito di fotogrammi B consecutivi tra I frame I e P.</span><span class="sxs-lookup"><span data-stu-id="aee02-104">Specifies the default number of consecutive B frames between I and P frames.</span></span>

<span data-ttu-id="aee02-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="aee02-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="aee02-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="aee02-106">Data type</span></span>

<span data-ttu-id="aee02-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="aee02-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aee02-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="aee02-108">Property GUID</span></span>

<span data-ttu-id="aee02-109">**Codecapis \_ AVEncMPVDefaultBPictureCount**</span><span class="sxs-lookup"><span data-stu-id="aee02-109">**CODECAPI\_AVEncMPVDefaultBPictureCount**</span></span>

## <a name="property-value"></a><span data-ttu-id="aee02-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aee02-110">Property value</span></span>

<span data-ttu-id="aee02-111">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="aee02-111">This property has a linear range of values.</span></span> <span data-ttu-id="aee02-112">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="aee02-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="aee02-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="aee02-113">Remarks</span></span>

<span data-ttu-id="aee02-114">Prima di Windows 8, questa proprietà si applica ai codificatori video MPEG.</span><span class="sxs-lookup"><span data-stu-id="aee02-114">Prior to Windows 8, this property applies to MPEG video encoders.</span></span> <span data-ttu-id="aee02-115">A partire da Windows 8, questa proprietà viene usata dai codificatori video MPEG, WMV e H. 264.</span><span class="sxs-lookup"><span data-stu-id="aee02-115">Starting with Windows 8, this property is used by MPEG, WMV, and H.264 video encoders.</span></span>

<span data-ttu-id="aee02-116">Se il codificatore supporta questa proprietà, può essere usato per controllare la struttura del Group of Pictures (GOP).</span><span class="sxs-lookup"><span data-stu-id="aee02-116">If the encoder supports this property, it can be used to control the group of pictures (GOP) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee02-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aee02-117">Requirements</span></span>



| <span data-ttu-id="aee02-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee02-118">Requirement</span></span> | <span data-ttu-id="aee02-119">Valore</span><span class="sxs-lookup"><span data-stu-id="aee02-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aee02-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aee02-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aee02-121">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="aee02-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aee02-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aee02-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aee02-123">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aee02-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aee02-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aee02-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee02-125"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="aee02-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee02-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aee02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee02-127">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="aee02-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="aee02-128">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="aee02-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




