---
description: Specifica il numero di sessioni di codifica completate. Questa proprietà si applica solo alla codifica Multipass.
ms.assetid: 19286f26-96f1-429c-9d6a-5e9b98597cd2
title: Proprietà AVEncStatCommonCompletedPasses (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2927e501963d450cbc08106e7860dfbfd2d7d98a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303929"
---
# <a name="avencstatcommoncompletedpasses-property"></a><span data-ttu-id="a4e8e-104">Proprietà AVEncStatCommonCompletedPasses</span><span class="sxs-lookup"><span data-stu-id="a4e8e-104">AVEncStatCommonCompletedPasses property</span></span>

<span data-ttu-id="a4e8e-105">Specifica il numero di sessioni di codifica completate.</span><span class="sxs-lookup"><span data-stu-id="a4e8e-105">Specifies the number of completed encoding passes.</span></span> <span data-ttu-id="a4e8e-106">Questa proprietà si applica solo alla codifica Multipass.</span><span class="sxs-lookup"><span data-stu-id="a4e8e-106">This property applies only to multi-pass encoding.</span></span>

<span data-ttu-id="a4e8e-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a4e8e-107">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4e8e-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a4e8e-108">Data type</span></span>

<span data-ttu-id="a4e8e-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a4e8e-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a4e8e-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="a4e8e-110">Property GUID</span></span>

<span data-ttu-id="a4e8e-111">**Codecapis \_ AVEncStatCommonCompletedPasses**</span><span class="sxs-lookup"><span data-stu-id="a4e8e-111">**CODECAPI\_AVEncStatCommonCompletedPasses**</span></span>

## <a name="property-value"></a><span data-ttu-id="a4e8e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a4e8e-112">Property value</span></span>

<span data-ttu-id="a4e8e-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="a4e8e-113">This property has a linear range of values.</span></span> <span data-ttu-id="a4e8e-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="a4e8e-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e8e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4e8e-115">Requirements</span></span>



| <span data-ttu-id="a4e8e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4e8e-116">Requirement</span></span> | <span data-ttu-id="a4e8e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a4e8e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e8e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4e8e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e8e-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a4e8e-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a4e8e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4e8e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e8e-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a4e8e-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a4e8e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4e8e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4e8e-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4e8e-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e8e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4e8e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e8e-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="a4e8e-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a4e8e-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a4e8e-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




