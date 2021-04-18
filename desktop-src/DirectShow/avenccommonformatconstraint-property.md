---
description: Specifica il formato di destinazione per un codificatore.
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: Proprietà AVEncCommonFormatConstraint (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e79536959aaaa0c50403bdd79d005bd48c729e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304246"
---
# <a name="avenccommonformatconstraint-property"></a><span data-ttu-id="64053-103">Proprietà AVEncCommonFormatConstraint</span><span class="sxs-lookup"><span data-stu-id="64053-103">AVEncCommonFormatConstraint property</span></span>

<span data-ttu-id="64053-104">Specifica il formato di destinazione per un codificatore.</span><span class="sxs-lookup"><span data-stu-id="64053-104">Specifies the target format for an encoder.</span></span>

<span data-ttu-id="64053-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="64053-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="64053-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="64053-106">Data type</span></span>

<span data-ttu-id="64053-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="64053-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="64053-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="64053-108">Property GUID</span></span>

<span data-ttu-id="64053-109">**Codecapis \_ AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="64053-109">**CODECAPI\_AVEncCommonFormatConstraint**</span></span>

## <a name="property-value"></a><span data-ttu-id="64053-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="64053-110">Property value</span></span>

<span data-ttu-id="64053-111">Il valore di questa proprietà è un **BSTR** che contiene la rappresentazione di stringa di un GUID.</span><span class="sxs-lookup"><span data-stu-id="64053-111">The value of this property is a **BSTR** that contains the string representation of a GUID.</span></span> <span data-ttu-id="64053-112">Sono definiti i seguenti GUID.</span><span class="sxs-lookup"><span data-stu-id="64053-112">The following GUIDs are defined.</span></span>



| <span data-ttu-id="64053-113">GUID</span><span class="sxs-lookup"><span data-stu-id="64053-113">GUID</span></span>                                         | <span data-ttu-id="64053-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64053-114">Description</span></span>                     |
|----------------------------------------------|---------------------------------|
| <span data-ttu-id="64053-115">\_GUID AVEncCommonFormatATSC di CODEcapi \_</span><span class="sxs-lookup"><span data-stu-id="64053-115">CODECAPI\_GUID\_AVEncCommonFormatATSC</span></span>        | <span data-ttu-id="64053-116">TV via cavo ATSC.</span><span class="sxs-lookup"><span data-stu-id="64053-116">ATSC cable television.</span></span>          |
| <span data-ttu-id="64053-117">\_GUID AVEncCommonFormatDVB di CODEcapi \_</span><span class="sxs-lookup"><span data-stu-id="64053-117">CODECAPI\_GUID\_AVEncCommonFormatDVB</span></span>         | <span data-ttu-id="64053-118">TV via cavo DVB.</span><span class="sxs-lookup"><span data-stu-id="64053-118">DVB cable television.</span></span>           |
| <span data-ttu-id="64053-119">GUID di codecapi \_ \_ AVEncCommonFormatDVD \_ DashVR</span><span class="sxs-lookup"><span data-stu-id="64053-119">CODECAPI\_GUID\_AVEncCommonFormatDVD\_DashVR</span></span> | <span data-ttu-id="64053-120">DVD-VR</span><span class="sxs-lookup"><span data-stu-id="64053-120">DVD-VR</span></span>                          |
| <span data-ttu-id="64053-121">GUID di codecapi \_ \_ AVEncCommonFormatDVD \_ PlusVR</span><span class="sxs-lookup"><span data-stu-id="64053-121">CODECAPI\_GUID\_AVEncCommonFormatDVD\_PlusVR</span></span> | <span data-ttu-id="64053-122">DVD + VR</span><span class="sxs-lookup"><span data-stu-id="64053-122">DVD+VR</span></span>                          |
| <span data-ttu-id="64053-123">GUID di codecapi \_ \_ AVEncCommonFormatDVD \_ V</span><span class="sxs-lookup"><span data-stu-id="64053-123">CODECAPI\_GUID\_AVEncCommonFormatDVD\_V</span></span>      | <span data-ttu-id="64053-124">DVD-Video</span><span class="sxs-lookup"><span data-stu-id="64053-124">DVD-Video</span></span>                       |
| <span data-ttu-id="64053-125">\_GUID AVEncCommonFormatHighMAT di CODEcapi \_</span><span class="sxs-lookup"><span data-stu-id="64053-125">CODECAPI\_GUID\_AVEncCommonFormatHighMAT</span></span>     | <span data-ttu-id="64053-126">HighMAT</span><span class="sxs-lookup"><span data-stu-id="64053-126">HighMAT</span></span>                         |
| <span data-ttu-id="64053-127">\_GUID AVEncCommonFormatHighMPV di CODEcapi \_</span><span class="sxs-lookup"><span data-stu-id="64053-127">CODECAPI\_GUID\_AVEncCommonFormatHighMPV</span></span>     | <span data-ttu-id="64053-128">Non documentato in questa versione.</span><span class="sxs-lookup"><span data-stu-id="64053-128">Not documented in this release.</span></span> |
| <span data-ttu-id="64053-129">\_GUID AVEncCommonFormatMP3 di CODEcapi \_</span><span class="sxs-lookup"><span data-stu-id="64053-129">CODECAPI\_GUID\_AVEncCommonFormatMP3</span></span>         | <span data-ttu-id="64053-130">Livello audio MPEG-3 (MP3)</span><span class="sxs-lookup"><span data-stu-id="64053-130">MPEG Audio Layer-3 (MP3)</span></span>        |
| <span data-ttu-id="64053-131">\_GUID AVEncCommonFormatSVCD di CODEcapi \_</span><span class="sxs-lookup"><span data-stu-id="64053-131">CODECAPI\_GUID\_AVEncCommonFormatSVCD</span></span>        | <span data-ttu-id="64053-132">CD con video Super (SVCD)</span><span class="sxs-lookup"><span data-stu-id="64053-132">Super Video CD (SVCD)</span></span>           |
| <span data-ttu-id="64053-133">\_GUID AVEncCommonFormatUnSpecified di CODEcapi \_</span><span class="sxs-lookup"><span data-stu-id="64053-133">CODECAPI\_GUID\_AVEncCommonFormatUnSpecified</span></span> | <span data-ttu-id="64053-134">Formato non specificato.</span><span class="sxs-lookup"><span data-stu-id="64053-134">Unspecified format.</span></span>             |
| <span data-ttu-id="64053-135">\_GUID AVEncCommonFormatVCD di CODEcapi \_</span><span class="sxs-lookup"><span data-stu-id="64053-135">CODECAPI\_GUID\_AVEncCommonFormatVCD</span></span>         | <span data-ttu-id="64053-136">CD video (VCD)</span><span class="sxs-lookup"><span data-stu-id="64053-136">Video CD (VCD)</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="64053-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="64053-137">Remarks</span></span>

<span data-ttu-id="64053-138">Le applicazioni possono impostare questa proprietà per specificare il formato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="64053-138">Applications can set this property to specify the target format.</span></span> <span data-ttu-id="64053-139">I codificatori possono inoltre restituire questa proprietà come funzionalità.</span><span class="sxs-lookup"><span data-stu-id="64053-139">Encoders can also return this property as a capability.</span></span>

## <a name="requirements"></a><span data-ttu-id="64053-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64053-140">Requirements</span></span>



| <span data-ttu-id="64053-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="64053-141">Requirement</span></span> | <span data-ttu-id="64053-142">Valore</span><span class="sxs-lookup"><span data-stu-id="64053-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64053-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64053-143">Minimum supported client</span></span><br/> | <span data-ttu-id="64053-144">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="64053-144">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="64053-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64053-145">Minimum supported server</span></span><br/> | <span data-ttu-id="64053-146">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="64053-146">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="64053-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64053-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="64053-148"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="64053-148"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64053-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64053-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64053-150">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="64053-150">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="64053-151">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="64053-151">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




