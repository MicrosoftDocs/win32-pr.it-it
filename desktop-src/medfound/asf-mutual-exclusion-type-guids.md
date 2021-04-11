---
description: I GUID seguenti definiscono i tipi per l'oggetto di esclusione reciproca per i flussi ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUID del tipo di esclusione reciproca ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225839"
---
# <a name="asf-mutual-exclusion-type-guids"></a><span data-ttu-id="35b0e-103">GUID del tipo di esclusione reciproca ASF</span><span class="sxs-lookup"><span data-stu-id="35b0e-103">ASF Mutual Exclusion Type GUIDs</span></span>

<span data-ttu-id="35b0e-104">I GUID seguenti definiscono i tipi per l'oggetto di esclusione reciproca per i flussi ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="35b0e-104">The following GUIDs define the types for the mutual exclusion object for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="35b0e-105">Costante</span><span class="sxs-lookup"><span data-stu-id="35b0e-105">Constant</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="35b0e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35b0e-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <span data-ttu-id="35b0e-107"><dt>**\_Lingua MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="35b0e-107"><dt>**MFASFMutexType\_Language**</dt></span></span> </dl>                 | <span data-ttu-id="35b0e-108">I flussi si escludono reciprocamente in base alla lingua.</span><span class="sxs-lookup"><span data-stu-id="35b0e-108">The streams are mutually exclusive by language.</span></span> <span data-ttu-id="35b0e-109">Questo tipo di esclusione reciproca è simile alle tracce audio di un DVD.</span><span class="sxs-lookup"><span data-stu-id="35b0e-109">This type of mutual exclusion is similar to the audio tracks on a DVD.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <span data-ttu-id="35b0e-110"><dt>**\_Velocità in bit MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="35b0e-110"><dt>**MFASFMutexType\_Bitrate**</dt></span></span> </dl>                     | <span data-ttu-id="35b0e-111">I flussi si escludono a vicenda in base alla velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="35b0e-111">The streams are mutually exclusive by bit rate.</span></span> <span data-ttu-id="35b0e-112">Questo tipo di esclusione reciproca viene anche definito esclusione di velocità in bit multipli (MBR).</span><span class="sxs-lookup"><span data-stu-id="35b0e-112">This type of mutual exclusion is also called multiple bit rate (MBR) exclusion.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <span data-ttu-id="35b0e-113"><dt>**Presentazione di MFASFMutexType \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35b0e-113"><dt>**MFASFMutexType\_Presentation**</dt></span></span> </dl> | <span data-ttu-id="35b0e-114">I flussi si escludono a vicenda dalla presentazione.</span><span class="sxs-lookup"><span data-stu-id="35b0e-114">The streams are mutually exclusive by presentation.</span></span> <span data-ttu-id="35b0e-115">Questo tipo può essere usato per molti scenari, ma deve essere usato solo quando il contenuto è lo stesso, ma assume un formato diverso.</span><span class="sxs-lookup"><span data-stu-id="35b0e-115">This type can be used for many scenarios, but it should only be used when the content is the same but takes a different form.</span></span> <span data-ttu-id="35b0e-116">Ad esempio, due flussi che contengono lo stesso video, uno formattato in modo da riempire lo schermo e l'altro che mantiene le proporzioni widescreen originali, devono essere resi esclusi a vicenda usando questo tipo.</span><span class="sxs-lookup"><span data-stu-id="35b0e-116">For example, two streams containing the same video, one formatted to fill the screen and the other maintaining the original widescreen aspect ratio, should be made mutually exclusive by using this type.</span></span> <span data-ttu-id="35b0e-117">Un altro esempio è costituito da flussi che contengono video della stessa scena ripresi da diverse angolazioni.</span><span class="sxs-lookup"><span data-stu-id="35b0e-117">Another example is streams containing video of the same scene shot from different angles.</span></span><br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <span data-ttu-id="35b0e-118"><dt>**MFASFMutexType \_ sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="35b0e-118"><dt>**MFASFMutexType\_Unknown**</dt></span></span> </dl>                     | <span data-ttu-id="35b0e-119">I flussi si escludono a vicenda in base a criteri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="35b0e-119">The streams are mutually exclusive based on custom criteria.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="35b0e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35b0e-120">Requirements</span></span>



| <span data-ttu-id="35b0e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="35b0e-121">Requirement</span></span> | <span data-ttu-id="35b0e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="35b0e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b0e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35b0e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="35b0e-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35b0e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="35b0e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35b0e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="35b0e-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35b0e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35b0e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35b0e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b0e-128"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b0e-128"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35b0e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35b0e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b0e-130">**IMFASFMutualExclusion:: GetType**</span><span class="sxs-lookup"><span data-stu-id="35b0e-130">**IMFASFMutualExclusion::GetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[<span data-ttu-id="35b0e-131">**IMFASFMutualExclusion:: seTYPE**</span><span class="sxs-lookup"><span data-stu-id="35b0e-131">**IMFASFMutualExclusion::SetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[<span data-ttu-id="35b0e-132">Costanti Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35b0e-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




