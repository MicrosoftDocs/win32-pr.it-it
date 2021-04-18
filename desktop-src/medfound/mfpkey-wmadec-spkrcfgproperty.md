---
description: Specifica la configurazione dell'altoparlante nel computer client.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: Proprietà MFPKEY_WMADEC_SPKRCFG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528567"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a><span data-ttu-id="9c82d-103">MFPKEY \_ WMADEC- \_ Proprietà SPKRCFG</span><span class="sxs-lookup"><span data-stu-id="9c82d-103">MFPKEY\_WMADEC\_SPKRCFG Property</span></span>

<span data-ttu-id="9c82d-104">Specifica la configurazione dell'altoparlante nel computer client.</span><span class="sxs-lookup"><span data-stu-id="9c82d-104">Specifies the speaker configuration on the client computer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9c82d-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9c82d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9c82d-106">g \_ wszWMACSpeakerConfig</span><span class="sxs-lookup"><span data-stu-id="9c82d-106">g\_wszWMACSpeakerConfig</span></span>

## <a name="data-type"></a><span data-ttu-id="9c82d-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9c82d-107">Data Type</span></span>

<span data-ttu-id="9c82d-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="9c82d-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="9c82d-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="9c82d-109">Default Value</span></span>

<span data-ttu-id="9c82d-110">Non viene presupposta alcuna configurazione specifica del altoparlante.</span><span class="sxs-lookup"><span data-stu-id="9c82d-110">No specific speaker configuration is assumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c82d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c82d-111">Remarks</span></span>

<span data-ttu-id="9c82d-112">È necessario impostare questo valore su una delle costanti o i valori indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9c82d-112">You should set this value to one of the constants or values in the following table.</span></span> <span data-ttu-id="9c82d-113">Le costanti sono definite in Microsoft DirectSound e sono elencate di seguito per praticità.</span><span class="sxs-lookup"><span data-stu-id="9c82d-113">The constants are defined in Microsoft DirectSound, and are listed here for convenience.</span></span> <span data-ttu-id="9c82d-114">Per risolvere questi nomi costanti per il compilatore, è necessario includere DSOUND. h.</span><span class="sxs-lookup"><span data-stu-id="9c82d-114">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="9c82d-115">Costante</span><span class="sxs-lookup"><span data-stu-id="9c82d-115">Constant</span></span>             | <span data-ttu-id="9c82d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9c82d-116">Value</span></span>      | <span data-ttu-id="9c82d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c82d-117">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9c82d-118">DSSPEAKER \_ diretto</span><span class="sxs-lookup"><span data-stu-id="9c82d-118">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="9c82d-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9c82d-119">0x00000000</span></span> | <span data-ttu-id="9c82d-120">L'audio viene passato direttamente, senza essere configurato per gli speaker.</span><span class="sxs-lookup"><span data-stu-id="9c82d-120">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="9c82d-121">\_cuffia DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="9c82d-121">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="9c82d-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9c82d-122">0x00000001</span></span> | <span data-ttu-id="9c82d-123">Il computer client è dotato di cuffie.</span><span class="sxs-lookup"><span data-stu-id="9c82d-123">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="9c82d-124">\_mono DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="9c82d-124">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="9c82d-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9c82d-125">0x00000002</span></span> | <span data-ttu-id="9c82d-126">Il computer client è dotato di un altoparlante Monoaural.</span><span class="sxs-lookup"><span data-stu-id="9c82d-126">The client computer is equipped with a monoaural speaker.</span></span>                    |
| <span data-ttu-id="9c82d-127">DSSPEAKER \_ quad</span><span class="sxs-lookup"><span data-stu-id="9c82d-127">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="9c82d-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="9c82d-128">0x00000003</span></span> | <span data-ttu-id="9c82d-129">Il computer client è dotato di altoparlanti quadrifonica.</span><span class="sxs-lookup"><span data-stu-id="9c82d-129">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="9c82d-130">DSSPEAKER \_ stereo</span><span class="sxs-lookup"><span data-stu-id="9c82d-130">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="9c82d-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9c82d-131">0x00000004</span></span> | <span data-ttu-id="9c82d-132">Il computer client è dotato di altoparlanti stereo.</span><span class="sxs-lookup"><span data-stu-id="9c82d-132">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="9c82d-133">DSSPEAKER \_ surround</span><span class="sxs-lookup"><span data-stu-id="9c82d-133">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="9c82d-134">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9c82d-134">0x00000005</span></span> | <span data-ttu-id="9c82d-135">Il computer client è dotato di altoparlanti con audio surround a quattro canali.</span><span class="sxs-lookup"><span data-stu-id="9c82d-135">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="9c82d-136">\_5POINT1 DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="9c82d-136">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="9c82d-137">0x00000006</span><span class="sxs-lookup"><span data-stu-id="9c82d-137">0x00000006</span></span> | <span data-ttu-id="9c82d-138">Il computer client è dotato di cinque altoparlanti e un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="9c82d-138">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="9c82d-139">\_7POINT1 DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="9c82d-139">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="9c82d-140">0x00000007</span><span class="sxs-lookup"><span data-stu-id="9c82d-140">0x00000007</span></span> | <span data-ttu-id="9c82d-141">Il computer client è dotato di sette altoparlanti e un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="9c82d-141">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="9c82d-142">Il valore impostato per questa proprietà determina i formati di output enumerati dal codec per l'audio multicanale.</span><span class="sxs-lookup"><span data-stu-id="9c82d-142">The value set for this property determines the output formats enumerated by the codec for multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c82d-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c82d-143">Requirements</span></span>



| <span data-ttu-id="9c82d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c82d-144">Requirement</span></span> | <span data-ttu-id="9c82d-145">Valore</span><span class="sxs-lookup"><span data-stu-id="9c82d-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c82d-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c82d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9c82d-147">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9c82d-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9c82d-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c82d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9c82d-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c82d-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c82d-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c82d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c82d-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c82d-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c82d-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c82d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c82d-153">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c82d-153">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




