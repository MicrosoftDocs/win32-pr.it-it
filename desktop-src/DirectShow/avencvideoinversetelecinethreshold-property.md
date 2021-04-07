---
description: Imposta la soglia in corrispondenza della quale il codificatore considera ridondante un campo video.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Proprietà AVEncVideoInverseTelecineThreshold (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745658"
---
# <a name="avencvideoinversetelecinethreshold-property"></a><span data-ttu-id="61b87-103">Proprietà AVEncVideoInverseTelecineThreshold</span><span class="sxs-lookup"><span data-stu-id="61b87-103">AVEncVideoInverseTelecineThreshold property</span></span>

<span data-ttu-id="61b87-104">Imposta la soglia in corrispondenza della quale il codificatore considera ridondante un campo video.</span><span class="sxs-lookup"><span data-stu-id="61b87-104">Sets the threshold at which the encoder considers a video field redundant.</span></span>

<span data-ttu-id="61b87-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="61b87-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="61b87-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="61b87-106">Data type</span></span>

<span data-ttu-id="61b87-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="61b87-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="61b87-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="61b87-108">Property GUID</span></span>

<span data-ttu-id="61b87-109">**Codecapis \_ AVEncVideoInverseTelecineThreshold**</span><span class="sxs-lookup"><span data-stu-id="61b87-109">**CODECAPI\_AVEncVideoInverseTelecineThreshold**</span></span>

## <a name="property-value"></a><span data-ttu-id="61b87-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="61b87-110">Property value</span></span>

<span data-ttu-id="61b87-111">Il valore di questa proprietà presenta l'intervallo seguente.</span><span class="sxs-lookup"><span data-stu-id="61b87-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="61b87-112">Valore</span><span class="sxs-lookup"><span data-stu-id="61b87-112">Value</span></span> | <span data-ttu-id="61b87-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61b87-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="61b87-114">0</span><span class="sxs-lookup"><span data-stu-id="61b87-114">0</span></span>     | <span data-ttu-id="61b87-115">È meno probabile che il codificatore prenda in considerazione i campi video ridondanti.</span><span class="sxs-lookup"><span data-stu-id="61b87-115">The encoder is less likely to consider video fields redundant.</span></span> |
| <span data-ttu-id="61b87-116">100</span><span class="sxs-lookup"><span data-stu-id="61b87-116">100</span></span>   | <span data-ttu-id="61b87-117">È più probabile che il codificatore prenda in considerazione i campi video ridondanti.</span><span class="sxs-lookup"><span data-stu-id="61b87-117">The encoder is more likely to consider video fields redundant.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="61b87-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="61b87-118">Remarks</span></span>

<span data-ttu-id="61b87-119">Impostare questa proprietà se il codificatore esegue una telecine inversa con un'origine video analoga.</span><span class="sxs-lookup"><span data-stu-id="61b87-119">Set this property if the encoder is performing inverse telecine with an analog video source.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b87-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61b87-120">Requirements</span></span>



| <span data-ttu-id="61b87-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b87-121">Requirement</span></span> | <span data-ttu-id="61b87-122">Valore</span><span class="sxs-lookup"><span data-stu-id="61b87-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61b87-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61b87-123">Minimum supported client</span></span><br/> | <span data-ttu-id="61b87-124">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="61b87-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="61b87-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61b87-125">Minimum supported server</span></span><br/> | <span data-ttu-id="61b87-126">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="61b87-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="61b87-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61b87-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b87-128"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="61b87-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b87-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61b87-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b87-130">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="61b87-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="61b87-131">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="61b87-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




