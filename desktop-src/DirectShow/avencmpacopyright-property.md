---
description: Specifica l'impostazione predefinita per il bit di copyright nel flusso audio MPEG-1. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Proprietà AVEncMPACopyright (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401278"
---
# <a name="avencmpacopyright-property"></a><span data-ttu-id="73e46-104">Proprietà AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="73e46-104">AVEncMPACopyright property</span></span>

<span data-ttu-id="73e46-105">Specifica l'impostazione predefinita per il bit di copyright nel flusso audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="73e46-105">Specifies the default setting for the copyright bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="73e46-106">Questa proprietà si applica ai codificatori audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="73e46-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="73e46-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="73e46-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="73e46-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="73e46-108">Data type</span></span>

<span data-ttu-id="73e46-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="73e46-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="73e46-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="73e46-110">Property GUID</span></span>

<span data-ttu-id="73e46-111">**Codecapis \_ AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="73e46-111">**CODECAPI\_AVEncMPACopyright**</span></span>

## <a name="property-value"></a><span data-ttu-id="73e46-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="73e46-112">Property value</span></span>

<span data-ttu-id="73e46-113">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="73e46-113">This property can have the following values.</span></span>



| <span data-ttu-id="73e46-114">Valore</span><span class="sxs-lookup"><span data-stu-id="73e46-114">Value</span></span>          | <span data-ttu-id="73e46-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73e46-115">Description</span></span>           |
|----------------|-----------------------|
| <span data-ttu-id="73e46-116">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="73e46-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="73e46-117">Il copyright è disattivato.</span><span class="sxs-lookup"><span data-stu-id="73e46-117">Copyright bit is off.</span></span> |
| <span data-ttu-id="73e46-118">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="73e46-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="73e46-119">Il copyright è il bit on.</span><span class="sxs-lookup"><span data-stu-id="73e46-119">Copyright bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="73e46-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="73e46-120">Remarks</span></span>

<span data-ttu-id="73e46-121">Il codificatore potrebbe eseguire l'override di questa impostazione, in base al contenuto del flusso di input.</span><span class="sxs-lookup"><span data-stu-id="73e46-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e46-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73e46-122">Requirements</span></span>



| <span data-ttu-id="73e46-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e46-123">Requirement</span></span> | <span data-ttu-id="73e46-124">Valore</span><span class="sxs-lookup"><span data-stu-id="73e46-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73e46-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73e46-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73e46-126">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="73e46-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="73e46-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73e46-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73e46-128">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="73e46-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="73e46-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73e46-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="73e46-130"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="73e46-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e46-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73e46-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e46-132">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="73e46-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="73e46-133">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="73e46-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




