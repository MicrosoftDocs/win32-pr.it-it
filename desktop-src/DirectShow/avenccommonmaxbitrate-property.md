---
description: Specifica la velocità in bit massima, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: Proprietà AVEncCommonMaxBitRate (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03844935e909591b2fe3c7244db79e77e7936f1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876898"
---
# <a name="avenccommonmaxbitrate-property"></a><span data-ttu-id="d631f-104">Proprietà AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="d631f-104">AVEncCommonMaxBitRate property</span></span>

<span data-ttu-id="d631f-105">Specifica la velocità in bit massima, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="d631f-105">Specifies the maximum bit rate, in bits per second.</span></span> <span data-ttu-id="d631f-106">Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="d631f-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="d631f-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d631f-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d631f-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d631f-108">Data type</span></span>

<span data-ttu-id="d631f-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d631f-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d631f-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="d631f-110">Property GUID</span></span>

<span data-ttu-id="d631f-111">**Codecapis \_ AVEncCommonMaxBitRate**</span><span class="sxs-lookup"><span data-stu-id="d631f-111">**CODECAPI\_AVEncCommonMaxBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="d631f-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d631f-112">Property value</span></span>

<span data-ttu-id="d631f-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="d631f-113">This property has a linear range of values.</span></span> <span data-ttu-id="d631f-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="d631f-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="d631f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d631f-115">Requirements</span></span>



| <span data-ttu-id="d631f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d631f-116">Requirement</span></span> | <span data-ttu-id="d631f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d631f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d631f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d631f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d631f-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="d631f-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d631f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d631f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d631f-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d631f-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d631f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d631f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d631f-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="d631f-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d631f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d631f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d631f-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="d631f-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d631f-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d631f-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




