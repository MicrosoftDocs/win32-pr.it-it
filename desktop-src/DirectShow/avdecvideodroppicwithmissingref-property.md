---
description: Specifica se il decodificatore rilascia i frame intra con frame di riferimento mancanti.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Proprietà AVDecVideoDropPicWithMissingRef (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225378"
---
# <a name="avdecvideodroppicwithmissingref-property"></a><span data-ttu-id="21584-103">Proprietà AVDecVideoDropPicWithMissingRef</span><span class="sxs-lookup"><span data-stu-id="21584-103">AVDecVideoDropPicWithMissingRef property</span></span>

<span data-ttu-id="21584-104">Specifica se il decodificatore rilascia i frame intra con frame di riferimento mancanti.</span><span class="sxs-lookup"><span data-stu-id="21584-104">Specifies whether the decoder drops intra frames with missing reference frames.</span></span>

<span data-ttu-id="21584-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="21584-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="21584-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="21584-106">Data type</span></span>

<span data-ttu-id="21584-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="21584-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="21584-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="21584-108">Property GUID</span></span>

<span data-ttu-id="21584-109">**Codecapis \_ AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="21584-109">**CODECAPI\_AVDecVideoDropPicWithMissingRef**</span></span>

## <a name="remarks"></a><span data-ttu-id="21584-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="21584-110">Remarks</span></span>

<span data-ttu-id="21584-111">Se il Bitstream è danneggiato, un frame potrebbe contenere frame di riferimento mancanti.</span><span class="sxs-lookup"><span data-stu-id="21584-111">If the bitstream is corrupted, a frame might have missing reference frames.</span></span> <span data-ttu-id="21584-112">Se il valore di questa proprietà è **Variant \_ true**, il decodificatore rilascia il frame.</span><span class="sxs-lookup"><span data-stu-id="21584-112">If the value of this property is **VARIANT\_TRUE**, the decoder drops the frame.</span></span> <span data-ttu-id="21584-113">Se il valore è **Variant \_ false**, il decodificatore tenta di decodificare il frame, utilizzando uno o più frame adiacenti come frame di riferimento.</span><span class="sxs-lookup"><span data-stu-id="21584-113">If the value is **VARIANT\_FALSE**, the decoder attempts to decode the frame, using one or more nearby frames as reference frames.</span></span> <span data-ttu-id="21584-114">Il frame decodificato risultante avrà elementi di blocco.</span><span class="sxs-lookup"><span data-stu-id="21584-114">The resulting decoded frame will have blocking artifacts.</span></span>

## <a name="requirements"></a><span data-ttu-id="21584-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21584-115">Requirements</span></span>



| <span data-ttu-id="21584-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="21584-116">Requirement</span></span> | <span data-ttu-id="21584-117">Valore</span><span class="sxs-lookup"><span data-stu-id="21584-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21584-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21584-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21584-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="21584-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="21584-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21584-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21584-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="21584-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="21584-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21584-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21584-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="21584-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21584-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21584-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21584-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="21584-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="21584-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="21584-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




