---
description: Specifica la velocità in bit minima, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Proprietà AVEncCommonMinBitRate (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c9b6e84675994d2aca7548f6c13d6558ebc020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304244"
---
# <a name="avenccommonminbitrate-property"></a><span data-ttu-id="3bdfe-104">Proprietà AVEncCommonMinBitRate</span><span class="sxs-lookup"><span data-stu-id="3bdfe-104">AVEncCommonMinBitRate property</span></span>

<span data-ttu-id="3bdfe-105">Specifica la velocità in bit minima, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-105">Specifies the minimum bit rate, in bits per second.</span></span> <span data-ttu-id="3bdfe-106">Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="3bdfe-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="3bdfe-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3bdfe-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3bdfe-108">Data type</span></span>

<span data-ttu-id="3bdfe-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="3bdfe-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3bdfe-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="3bdfe-110">Property GUID</span></span>

<span data-ttu-id="3bdfe-111">**Codecapis \_ AVEncCommonMinBitRate**</span><span class="sxs-lookup"><span data-stu-id="3bdfe-111">**CODECAPI\_AVEncCommonMinBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="3bdfe-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3bdfe-112">Property value</span></span>

<span data-ttu-id="3bdfe-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-113">This property has a linear range of values.</span></span> <span data-ttu-id="3bdfe-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="3bdfe-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="3bdfe-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bdfe-115">Remarks</span></span>

<span data-ttu-id="3bdfe-116">Il codificatore impone la velocità in bit minima aumentando la qualità della codifica in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="3bdfe-116">The encoder enforces the minimum bit rate by increasing the encoding quality as necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bdfe-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bdfe-117">Requirements</span></span>



| <span data-ttu-id="3bdfe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bdfe-118">Requirement</span></span> | <span data-ttu-id="3bdfe-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3bdfe-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bdfe-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bdfe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3bdfe-121">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="3bdfe-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3bdfe-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bdfe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3bdfe-123">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3bdfe-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3bdfe-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bdfe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bdfe-125"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bdfe-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bdfe-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bdfe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bdfe-127">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="3bdfe-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3bdfe-128">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="3bdfe-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




