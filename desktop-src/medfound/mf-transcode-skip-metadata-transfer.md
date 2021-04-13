---
description: Specifica se i metadati vengono scritti nel file transcodificato.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Attributo MF_TRANSCODE_SKIP_METADATA_TRANSFER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226373"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a><span data-ttu-id="68893-103">\_Attributo per il \_ \_ trasferimento dei metadati con MF transcode Skip \_</span><span class="sxs-lookup"><span data-stu-id="68893-103">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute</span></span>

<span data-ttu-id="68893-104">Specifica se i metadati vengono scritti nel file transcodificato.</span><span class="sxs-lookup"><span data-stu-id="68893-104">Specifies whether metadata is written to the transcoded file.</span></span> <span data-ttu-id="68893-105">Questo attributo del contenitore viene archiviato nel profilo transcodifica.</span><span class="sxs-lookup"><span data-stu-id="68893-105">This container attribute is stored in the transcode profile.</span></span>

## <a name="data-type"></a><span data-ttu-id="68893-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="68893-106">Data type</span></span>

<span data-ttu-id="68893-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="68893-107">**UINT32**</span></span>

<span data-ttu-id="68893-108">\_ \_ \_ Nella tabella seguente sono descritti i valori possibili per l'attributo MF transcode Skip Metadata \_ transfer.</span><span class="sxs-lookup"><span data-stu-id="68893-108">Possible values for the MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute are described in the following table.</span></span>



| <span data-ttu-id="68893-109">Valore</span><span class="sxs-lookup"><span data-stu-id="68893-109">Value</span></span>                                                                        | <span data-ttu-id="68893-110">Significato</span><span class="sxs-lookup"><span data-stu-id="68893-110">Meaning</span></span>                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68893-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68893-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="68893-112">Trasferisce automaticamente i metadati a livello di file dal file di origine al file transcodificato.</span><span class="sxs-lookup"><span data-stu-id="68893-112">Automatically transfers file-level metadata from the source file to the transcoded file.</span></span><br/> |
| <dl> <span data-ttu-id="68893-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="68893-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="68893-114">I metadati del file di origine non vengono scritti nel file transcodificato.</span><span class="sxs-lookup"><span data-stu-id="68893-114">The source file metadata is not written to the transcoded file.</span></span><br/>                          |



 

## <a name="getset"></a><span data-ttu-id="68893-115">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="68893-115">Get/set</span></span>

<span data-ttu-id="68893-116">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="68893-116">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="68893-117">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="68893-117">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="68893-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="68893-118">Remarks</span></span>

<span data-ttu-id="68893-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="68893-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68893-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68893-120">Requirements</span></span>



| <span data-ttu-id="68893-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="68893-121">Requirement</span></span> | <span data-ttu-id="68893-122">Valore</span><span class="sxs-lookup"><span data-stu-id="68893-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68893-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68893-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68893-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="68893-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="68893-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68893-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68893-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="68893-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="68893-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68893-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68893-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68893-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68893-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68893-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68893-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68893-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68893-131">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="68893-131">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="68893-132">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="68893-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




