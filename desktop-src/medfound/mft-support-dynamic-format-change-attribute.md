---
description: Specifica se una trasformazione Media Foundation (MFT) supporta le modifiche al formato dinamico.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: Attributo MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310209"
---
# <a name="mft_support_dynamic_format_change-attribute"></a><span data-ttu-id="3489e-103">L' \_ \_ attributo di \_ modifica del formato dinamico del supporto MFT \_</span><span class="sxs-lookup"><span data-stu-id="3489e-103">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE attribute</span></span>

<span data-ttu-id="3489e-104">Specifica se una trasformazione Media Foundation (MFT) supporta le modifiche al formato dinamico.</span><span class="sxs-lookup"><span data-stu-id="3489e-104">Specifies whether a Media Foundation transform (MFT) supports dynamic format changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="3489e-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3489e-105">Data type</span></span>

<span data-ttu-id="3489e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3489e-106">**UINT32**</span></span>

<span data-ttu-id="3489e-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="3489e-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3489e-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="3489e-108">Remarks</span></span>

<span data-ttu-id="3489e-109">Questo attributo può avere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3489e-109">This attribute can have the following values.</span></span>



| <span data-ttu-id="3489e-110">Valore</span><span class="sxs-lookup"><span data-stu-id="3489e-110">Value</span></span>     | <span data-ttu-id="3489e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3489e-111">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="3489e-112">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="3489e-112">**TRUE**</span></span>  | <span data-ttu-id="3489e-113">Il client può modificare il formato di input durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="3489e-113">The client can change the input format during streaming.</span></span>               |
| <span data-ttu-id="3489e-114">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="3489e-114">**FALSE**</span></span> | <span data-ttu-id="3489e-115">Il MFT deve essere svuotato prima che il client possa modificare il formato di input.</span><span class="sxs-lookup"><span data-stu-id="3489e-115">The MFT must be drained before the client can change the input format.</span></span> |



 

<span data-ttu-id="3489e-116">Per ottenere questo attributo, chiamare prima [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi globale per MFT.</span><span class="sxs-lookup"><span data-stu-id="3489e-116">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store for the MFT.</span></span> <span data-ttu-id="3489e-117">Chiamare quindi [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="3489e-117">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span>

<span data-ttu-id="3489e-118">Se [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) ha esito negativo o se l'attributo non è presente, il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="3489e-118">If [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fails or the attribute is not present, the default value if **FALSE**.</span></span>

<span data-ttu-id="3489e-119">[MFTS asincrono](asynchronous-mfts.md) deve restituire il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="3489e-119">[Asynchronous MFTs](asynchronous-mfts.md) must return the value **TRUE**.</span></span>

<span data-ttu-id="3489e-120">Per ulteriori informazioni, vedere [gestione delle modifiche al flusso](handling-stream-changes.md).</span><span class="sxs-lookup"><span data-stu-id="3489e-120">For more information, see [Handling Stream Changes](handling-stream-changes.md).</span></span>

<span data-ttu-id="3489e-121">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3489e-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3489e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3489e-122">Requirements</span></span>



| <span data-ttu-id="3489e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3489e-123">Requirement</span></span> | <span data-ttu-id="3489e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3489e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3489e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3489e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3489e-126">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3489e-126">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="3489e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3489e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3489e-128">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="3489e-128">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3489e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3489e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3489e-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3489e-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3489e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3489e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3489e-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3489e-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3489e-133">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="3489e-133">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="3489e-134">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="3489e-134">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="3489e-135">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="3489e-135">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3489e-136">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="3489e-136">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3489e-137">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="3489e-137">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




