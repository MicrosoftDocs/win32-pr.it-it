---
description: Specifica il livello di alimentazione per il decodificatore.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: Proprietà MFPKEY_AVDecVideoSWPowerLevel (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307955"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a><span data-ttu-id="6f985-103">\_Proprietà AVDecVideoSWPowerLevel di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="6f985-103">MFPKEY\_AVDecVideoSWPowerLevel Property</span></span>

<span data-ttu-id="6f985-104">Specifica il livello di alimentazione per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="6f985-104">Specifies the power level for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="6f985-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="6f985-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="6f985-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="6f985-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="6f985-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6f985-107">Data Type</span></span>

<span data-ttu-id="6f985-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="6f985-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="6f985-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="6f985-109">Default Value</span></span>

<span data-ttu-id="6f985-110">**100**</span><span class="sxs-lookup"><span data-stu-id="6f985-110">**100**</span></span>

## <a name="remarks"></a><span data-ttu-id="6f985-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f985-111">Remarks</span></span>

<span data-ttu-id="6f985-112">Questa proprietà deve essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6f985-112">This property must be set to one of the following values.</span></span>



| <span data-ttu-id="6f985-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6f985-113">Value</span></span> | <span data-ttu-id="6f985-114">Significato</span><span class="sxs-lookup"><span data-stu-id="6f985-114">Meaning</span></span>                                                             |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="6f985-115">0</span><span class="sxs-lookup"><span data-stu-id="6f985-115">0</span></span>     | <span data-ttu-id="6f985-116">Il decodificatore usa un livello di alimentazione ottimizzato per la durata della batteria.</span><span class="sxs-lookup"><span data-stu-id="6f985-116">The decoder uses a power level that is optimized for battery life.</span></span>  |
| <span data-ttu-id="6f985-117">50</span><span class="sxs-lookup"><span data-stu-id="6f985-117">50</span></span>    | <span data-ttu-id="6f985-118">Il decodificatore usa un livello di risparmio energia bilanciato.</span><span class="sxs-lookup"><span data-stu-id="6f985-118">The decoder uses a balanced power level.</span></span>                            |
| <span data-ttu-id="6f985-119">100</span><span class="sxs-lookup"><span data-stu-id="6f985-119">100</span></span>   | <span data-ttu-id="6f985-120">Il decodificatore usa un livello di alimentazione ottimizzato per la qualità del video.</span><span class="sxs-lookup"><span data-stu-id="6f985-120">The decoder uses a power level that is optimized for video quality.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6f985-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f985-121">Requirements</span></span>



| <span data-ttu-id="6f985-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f985-122">Requirement</span></span> | <span data-ttu-id="6f985-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6f985-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f985-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f985-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f985-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6f985-125">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6f985-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f985-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f985-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f985-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6f985-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f985-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f985-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f985-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f985-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f985-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f985-131">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f985-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
