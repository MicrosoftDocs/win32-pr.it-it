---
description: Specifica il modo in cui il flusso video decodificato è interlacciato.
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: Proprietà AVDecVideoInputScanType (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876778"
---
# <a name="avdecvideoinputscantype-property"></a><span data-ttu-id="83e72-103">Proprietà AVDecVideoInputScanType</span><span class="sxs-lookup"><span data-stu-id="83e72-103">AVDecVideoInputScanType property</span></span>

<span data-ttu-id="83e72-104">Specifica il modo in cui il flusso video decodificato è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="83e72-104">Specifies how the decoded video stream is interlaced.</span></span>

<span data-ttu-id="83e72-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="83e72-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="83e72-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="83e72-106">Data type</span></span>

<span data-ttu-id="83e72-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="83e72-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="83e72-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="83e72-108">Property GUID</span></span>

<span data-ttu-id="83e72-109">**Codecapis \_ AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="83e72-109">**CODECAPI\_AVDecVideoInputScanType**</span></span>

## <a name="property-value"></a><span data-ttu-id="83e72-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="83e72-110">Property value</span></span>

<span data-ttu-id="83e72-111">Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) .</span><span class="sxs-lookup"><span data-stu-id="83e72-111">The value of this property is a member of the [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="83e72-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="83e72-112">Remarks</span></span>

<span data-ttu-id="83e72-113">I 16 bit superiori del valore contengono la larghezza e i 16 bit inferiori contengono l'altezza.</span><span class="sxs-lookup"><span data-stu-id="83e72-113">The upper 16 bits of the value contain the width, and the lower 16 bits contain the height.</span></span>

## <a name="requirements"></a><span data-ttu-id="83e72-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83e72-114">Requirements</span></span>



| <span data-ttu-id="83e72-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e72-115">Requirement</span></span> | <span data-ttu-id="83e72-116">Valore</span><span class="sxs-lookup"><span data-stu-id="83e72-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83e72-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83e72-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83e72-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="83e72-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="83e72-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83e72-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83e72-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="83e72-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="83e72-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83e72-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="83e72-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="83e72-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83e72-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83e72-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e72-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="83e72-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="83e72-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="83e72-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

