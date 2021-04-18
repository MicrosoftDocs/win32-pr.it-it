---
description: Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Proprietà AVEncMPAEnableRedundancyProtection (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304148"
---
# <a name="avencmpaenableredundancyprotection-property"></a><span data-ttu-id="7b790-104">Proprietà AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="7b790-104">AVEncMPAEnableRedundancyProtection property</span></span>

<span data-ttu-id="7b790-105">Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame.</span><span class="sxs-lookup"><span data-stu-id="7b790-105">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span> <span data-ttu-id="7b790-106">Questa proprietà si applica ai codificatori audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="7b790-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="7b790-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7b790-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7b790-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7b790-108">Data type</span></span>

<span data-ttu-id="7b790-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="7b790-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7b790-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="7b790-110">Property GUID</span></span>

<span data-ttu-id="7b790-111">**Codecapis \_ AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="7b790-111">**CODECAPI\_AVEncMPAEnableRedundancyProtection**</span></span>

## <a name="property-value"></a><span data-ttu-id="7b790-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7b790-112">Property value</span></span>

<span data-ttu-id="7b790-113">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b790-113">This property can have the following values.</span></span>



| <span data-ttu-id="7b790-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7b790-114">Value</span></span>          | <span data-ttu-id="7b790-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b790-115">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="7b790-116">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="7b790-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="7b790-117">Non aggiungere un checksum CRC.</span><span class="sxs-lookup"><span data-stu-id="7b790-117">Do not add a CRC checksum.</span></span> |
| <span data-ttu-id="7b790-118">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="7b790-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="7b790-119">Aggiungere un checksum CRC.</span><span class="sxs-lookup"><span data-stu-id="7b790-119">Add a CRC checksum.</span></span>        |



 

## <a name="requirements"></a><span data-ttu-id="7b790-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b790-120">Requirements</span></span>



| <span data-ttu-id="7b790-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b790-121">Requirement</span></span> | <span data-ttu-id="7b790-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7b790-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b790-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b790-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7b790-124">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="7b790-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7b790-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b790-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7b790-126">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7b790-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7b790-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b790-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b790-128"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b790-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b790-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b790-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b790-130">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="7b790-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7b790-131">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="7b790-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




