---
description: Specifica la matrice di quantizzazione Luma per macroblocchi non intra. Questa proprietà si applica ai codificatori video MPEG.
ms.assetid: 087e47c1-2a8a-4687-85c1-ac18708174e1
title: Proprietà AVEncMPVQuantMatrixNonIntra (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb70fa38d263365d9de2890be9756b46e09547ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480949"
---
# <a name="avencmpvquantmatrixnonintra-property"></a><span data-ttu-id="584cb-104">Proprietà AVEncMPVQuantMatrixNonIntra</span><span class="sxs-lookup"><span data-stu-id="584cb-104">AVEncMPVQuantMatrixNonIntra property</span></span>

<span data-ttu-id="584cb-105">Specifica la matrice di quantizzazione Luma per macroblocchi non intra.</span><span class="sxs-lookup"><span data-stu-id="584cb-105">Specifies the luma quantization matrix for non-intra macroblocks.</span></span> <span data-ttu-id="584cb-106">Questa proprietà si applica ai codificatori video MPEG.</span><span class="sxs-lookup"><span data-stu-id="584cb-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="584cb-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="584cb-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="584cb-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="584cb-108">Data type</span></span>

<span data-ttu-id="584cb-109">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="584cb-109">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="584cb-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="584cb-110">Property GUID</span></span>

<span data-ttu-id="584cb-111">**Codecapis \_ AVEncMPVQuantMatrixNonIntra**</span><span class="sxs-lookup"><span data-stu-id="584cb-111">**CODECAPI\_AVEncMPVQuantMatrixNonIntra**</span></span>

## <a name="property-value"></a><span data-ttu-id="584cb-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="584cb-112">Property value</span></span>

<span data-ttu-id="584cb-113">Il valore di questa proprietà è una stringa che contiene i coefficienti a 64 8 bit codificati come stringa di valori esadecimali (128 caratteri).</span><span class="sxs-lookup"><span data-stu-id="584cb-113">The value of this property is a string that contains the 64 8-bit coefficients encoded as a string of hexadecimal values (128 characters).</span></span>

## <a name="requirements"></a><span data-ttu-id="584cb-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="584cb-114">Requirements</span></span>



| <span data-ttu-id="584cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="584cb-115">Requirement</span></span> | <span data-ttu-id="584cb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="584cb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="584cb-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="584cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="584cb-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="584cb-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="584cb-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="584cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="584cb-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="584cb-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="584cb-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="584cb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="584cb-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="584cb-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="584cb-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="584cb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584cb-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="584cb-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="584cb-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="584cb-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




