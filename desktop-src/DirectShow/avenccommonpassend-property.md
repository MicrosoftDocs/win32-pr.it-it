---
description: Arresta il passaggio di codifica corrente o esegue una query se il passaggio di codifica corrente è l'ultimo.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Proprietà AVEncCommonPassEnd (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482516"
---
# <a name="avenccommonpassend-property"></a><span data-ttu-id="6660b-103">Proprietà AVEncCommonPassEnd</span><span class="sxs-lookup"><span data-stu-id="6660b-103">AVEncCommonPassEnd property</span></span>

<span data-ttu-id="6660b-104">Arresta il passaggio di codifica corrente o esegue una query se il passaggio di codifica corrente è l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="6660b-104">Stops the current encoding pass, or queries whether the current encoding pass is the last one.</span></span>

<span data-ttu-id="6660b-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6660b-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6660b-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6660b-106">Data type</span></span>

<span data-ttu-id="6660b-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="6660b-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6660b-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="6660b-108">Property GUID</span></span>

<span data-ttu-id="6660b-109">**Codecapis \_ AVEncCommonPassEnd**</span><span class="sxs-lookup"><span data-stu-id="6660b-109">**CODECAPI\_AVEncCommonPassEnd**</span></span>

## <a name="remarks"></a><span data-ttu-id="6660b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6660b-110">Remarks</span></span>

<span data-ttu-id="6660b-111">L'impostazione di questa proprietà su **Variant \_ true** termina il passaggio di codifica corrente.</span><span class="sxs-lookup"><span data-stu-id="6660b-111">Setting this property to **VARIANT\_TRUE** ends the current encoding pass.</span></span> <span data-ttu-id="6660b-112">Se si imposta questa proprietà su **Variant \_ false** , viene terminata la codifica Multipass.</span><span class="sxs-lookup"><span data-stu-id="6660b-112">Setting this property to **VARIANT\_FALSE** terminates multipass encoding.</span></span>

<span data-ttu-id="6660b-113">La lettura di questa proprietà esegue una query se il passaggio di codifica corrente è l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="6660b-113">Reading this property queries whether the current encoding pass is the last one.</span></span>

## <a name="requirements"></a><span data-ttu-id="6660b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6660b-114">Requirements</span></span>



| <span data-ttu-id="6660b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6660b-115">Requirement</span></span> | <span data-ttu-id="6660b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6660b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6660b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6660b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6660b-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="6660b-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6660b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6660b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6660b-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6660b-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6660b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6660b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6660b-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="6660b-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6660b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6660b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6660b-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="6660b-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6660b-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6660b-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




