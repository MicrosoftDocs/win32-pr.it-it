---
description: Specifica per una topologia transcodificata se il caricatore della topologia caricherà le trasformazioni basate su hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: Attributo MF_TRANSCODE_TOPOLOGYMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879814"
---
# <a name="mf_transcode_topologymode-attribute"></a><span data-ttu-id="0ca7c-103">\_Attributo transcode \_ TOPOLOGYMODE MF</span><span class="sxs-lookup"><span data-stu-id="0ca7c-103">MF\_TRANSCODE\_TOPOLOGYMODE attribute</span></span>

<span data-ttu-id="0ca7c-104">Specifica per una topologia transcodificata se il caricatore della topologia caricherà le trasformazioni basate su hardware.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-104">Specifies for a transcode topology whether the topology loader will load hardware-based transforms.</span></span>

<span data-ttu-id="0ca7c-105">La modalità topologia specifica se è possibile utilizzare le trasformazioni hardware (ad esempio, i codec hardware) nella topologia transcodifica.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-105">The topology mode specifies whether hardware transforms (such as hardware codecs) may be used in the transcode topology.</span></span> <span data-ttu-id="0ca7c-106">L'applicazione può archiviare questo attributo in un profilo transcode chiamando [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="0ca7c-106">The application can store this attribute in a transcode profile by calling [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span>

## <a name="data-type"></a><span data-ttu-id="0ca7c-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0ca7c-107">Data type</span></span>

<span data-ttu-id="0ca7c-108">**[**MF \_ Transcodificare i \_ \_ flag TOPOLOGYMODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** archiviati come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ca7c-108">**[**MF\_TRANSCODE\_TOPOLOGYMODE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0ca7c-109">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="0ca7c-109">Get/set</span></span>

<span data-ttu-id="0ca7c-110">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0ca7c-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0ca7c-111">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ca7c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ca7c-112">Remarks</span></span>

<span data-ttu-id="0ca7c-113">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-113">This attribute is optional.</span></span> <span data-ttu-id="0ca7c-114">Deve avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-114">It must have one of the following values.</span></span>



| <span data-ttu-id="0ca7c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0ca7c-115">Value</span></span>                                              | <span data-ttu-id="0ca7c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ca7c-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca7c-117">**MF \_ transcode \_ TOPOLOGYMODE \_ hardware \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="0ca7c-117">**MF\_TRANSCODE\_TOPOLOGYMODE\_HARDWARE\_ALLOWED**</span></span> | <span data-ttu-id="0ca7c-118">Il caricatore della topologia caricherà i MFTs basati su hardware, ad esempio i decodificatori hardware, quando disponibili.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="0ca7c-119">Il caricatore della topologia esegue automaticamente il fallback alla decodifica software se non viene trovato alcun decodificatore hardware o se un decodificatore hardware non riesce a connettersi per qualche motivo.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="0ca7c-120">**MF \_ transcode \_ TOPOLOGYMODE \_ \_ solo software**</span><span class="sxs-lookup"><span data-stu-id="0ca7c-120">**MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**</span></span>    | <span data-ttu-id="0ca7c-121">Il caricatore della topologia caricherà solo MFTs software, inclusi i decodificatori software.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="0ca7c-122">Il valore predefinito è **MF \_ transcode \_ TOPOLOGYMODE \_ \_ solo software**.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-122">The default value is **MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**.</span></span>

<span data-ttu-id="0ca7c-123">Se il caricatore della topologia inserisce una MFT hardware nella topologia, imposta l'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) nel nodo della topologia.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-123">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="0ca7c-124">Per verificare se è presente un hardware MFT, enumerare i nodi nella topologia risolta e verificare se questo attributo è presente.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-124">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="0ca7c-125">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0ca7c-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca7c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ca7c-126">Requirements</span></span>



| <span data-ttu-id="0ca7c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ca7c-127">Requirement</span></span> | <span data-ttu-id="0ca7c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0ca7c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca7c-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ca7c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca7c-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0ca7c-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0ca7c-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ca7c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca7c-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ca7c-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0ca7c-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ca7c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ca7c-134"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ca7c-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca7c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ca7c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca7c-136">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0ca7c-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ca7c-137">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="0ca7c-137">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="0ca7c-138">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="0ca7c-138">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="0ca7c-139">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="0ca7c-139">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




