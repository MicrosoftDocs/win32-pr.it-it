---
description: Abilita o Disabilita il read-ahead in un'origine multimediale.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: Proprietà MFPKEY_MediaSource_DisableReadAhead (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328190"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a><span data-ttu-id="e645d-103">\_ \_ Proprietà DISABLEREADAHEAD di MFPKEY MediaSource</span><span class="sxs-lookup"><span data-stu-id="e645d-103">MFPKEY\_MediaSource\_DisableReadAhead property</span></span>

<span data-ttu-id="e645d-104">Abilita o Disabilita il read-ahead in un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="e645d-104">Enables or disables read-ahead in a media source.</span></span>



<span data-ttu-id="e645d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e645d-105">Data type</span></span>

<span data-ttu-id="e645d-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e645d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e645d-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e645d-107">PROPVARIANT member</span></span>

<span data-ttu-id="e645d-108">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="e645d-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="e645d-109">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="e645d-109">VT\_BOOL</span></span>

<span data-ttu-id="e645d-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="e645d-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e645d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e645d-111">Remarks</span></span>

<span data-ttu-id="e645d-112">Le applicazioni possono usare questa proprietà per configurare alcune origini multimediali.</span><span class="sxs-lookup"><span data-stu-id="e645d-112">Applications can use this property to configure some media sources.</span></span> <span data-ttu-id="e645d-113">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="e645d-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="e645d-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e645d-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="e645d-115">Se il valore è **Variant \_ true**, l'origine multimediale non verrà letta in anticipo nel flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="e645d-115">If the value is **VARIANT\_TRUE**, the media source will not read ahead in the byte stream.</span></span> <span data-ttu-id="e645d-116">Questa impostazione può ottimizzare le prestazioni se si prevede di leggere una quantità limitata di dati dall'origine multimediale, ad esempio per ottenere un'immagine di anteprima da un file video.</span><span class="sxs-lookup"><span data-stu-id="e645d-116">This setting can optimize performance if you plan to read a limited amount of data from the media source—for example, to get a thumbnail image from a video file.</span></span>

<span data-ttu-id="e645d-117">Per la riproduzione audio/video tipica, questa proprietà deve essere impostata su **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e645d-117">For typical audio/video playback, this property should be set to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="e645d-118">Il valore predefinito è **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e645d-118">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="e645d-119">Non ogni origine supporto supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="e645d-119">Not every media source supports this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e645d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e645d-120">Requirements</span></span>



| <span data-ttu-id="e645d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e645d-121">Requirement</span></span> | <span data-ttu-id="e645d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e645d-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e645d-123">Client</span><span class="sxs-lookup"><span data-stu-id="e645d-123">Client</span></span><br/> | <span data-ttu-id="e645d-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e645d-124">Windows 7</span></span><br/>                                                               |
| <span data-ttu-id="e645d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e645d-125">Header</span></span><br/> | <dl> <span data-ttu-id="e645d-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e645d-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e645d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e645d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e645d-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e645d-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




