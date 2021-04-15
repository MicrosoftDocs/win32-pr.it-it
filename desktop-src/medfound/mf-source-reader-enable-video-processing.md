---
description: Consente l'elaborazione video da parte del lettore di origine.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: Attributo MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484805"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a><span data-ttu-id="e4a59-103">MF \_ source \_ Reader \_ Abilita \_ l' \_ attributo elaborazione video</span><span class="sxs-lookup"><span data-stu-id="e4a59-103">MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="e4a59-104">Consente l'elaborazione video da parte del [lettore di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="e4a59-104">Enables video processing by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="e4a59-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e4a59-105">Data type</span></span>

<span data-ttu-id="e4a59-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e4a59-106">**UINT32**</span></span>



| <span data-ttu-id="e4a59-107">Valore</span><span class="sxs-lookup"><span data-stu-id="e4a59-107">Value</span></span>                                                                                                                                                                | <span data-ttu-id="e4a59-108">Significato</span><span class="sxs-lookup"><span data-stu-id="e4a59-108">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <span data-ttu-id="e4a59-109"><dt>**Diverso da zero**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a59-109"><dt>**Nonzero**</dt></span></span> </dl> | <span data-ttu-id="e4a59-110">Abilitare l'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="e4a59-110">Enable video processing.</span></span><br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <span data-ttu-id="e4a59-111"><dt>**Zero**</dt></span><span class="sxs-lookup"><span data-stu-id="e4a59-111"><dt>**Zero**</dt></span></span> </dl>             | <span data-ttu-id="e4a59-112">Disabilitare l'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="e4a59-112">Disable video processing.</span></span> <span data-ttu-id="e4a59-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e4a59-113">(Default)</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="e4a59-114">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="e4a59-114">Get/set</span></span>

<span data-ttu-id="e4a59-115">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e4a59-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e4a59-116">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="e4a59-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a59-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4a59-117">Remarks</span></span>

<span data-ttu-id="e4a59-118">Se questo attributo è **true** (diverso da zero), il lettore di origine può eseguire l'elaborazione video limitata seguente nei fotogrammi video non compressi:</span><span class="sxs-lookup"><span data-stu-id="e4a59-118">If this attribute is **TRUE** (nonzero), the source reader can perform the following limited video processing on uncompressed video frames:</span></span>

-   <span data-ttu-id="e4a59-119">Conversione da YUV a RGB-32.</span><span class="sxs-lookup"><span data-stu-id="e4a59-119">Conversion from YUV to RGB-32.</span></span>
-   <span data-ttu-id="e4a59-120">Deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="e4a59-120">Deinterlacing.</span></span>

<span data-ttu-id="e4a59-121">Queste operazioni vengono eseguite nel software e non sono ottimizzate per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e4a59-121">These operations are performed in software, and are not optimized for playback.</span></span> <span data-ttu-id="e4a59-122">Questa funzionalità è destinata alle applicazioni che elaborano un numero ridotto di frame, ad esempio per creare un'anteprima video, o applicazioni che non decodificano i frame in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="e4a59-122">This feature is intended for applications that process a small number of frames—for example, to create a video thumbnail—or applications that do not decode frames in real time.</span></span> <span data-ttu-id="e4a59-123">L'operazione di deinterlacciamento esegue l'interpolazione dei dati da un singolo campo, in modo da avere un valore loss.</span><span class="sxs-lookup"><span data-stu-id="e4a59-123">The deinterlace operation interpolates data from a single field, so it is lossy.</span></span>

<span data-ttu-id="e4a59-124">Evitare questa impostazione se si utilizza Direct3D per visualizzare i fotogrammi video, perché la GPU offre in genere migliori funzionalità di elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="e4a59-124">Avoid this setting if you are using Direct3D to display the video frames, because the GPU generally provides better video processing capabilities.</span></span>

<span data-ttu-id="e4a59-125">Se questo attributo è **true**, i seguenti attributi devono essere **false**:</span><span class="sxs-lookup"><span data-stu-id="e4a59-125">If this attribute is **TRUE**, the following attributes must be **FALSE**:</span></span>

-   [<span data-ttu-id="e4a59-126">\_ \_ Gestione D3D del lettore di origine MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="e4a59-126">MF\_SOURCE\_READER\_D3D\_MANAGER</span></span>](mf-source-reader-d3d-manager.md)
-   [<span data-ttu-id="e4a59-127">MF \_ ReadWrite \_ Disabilita \_ convertitori</span><span class="sxs-lookup"><span data-stu-id="e4a59-127">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)

## <a name="requirements"></a><span data-ttu-id="e4a59-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4a59-128">Requirements</span></span>



| <span data-ttu-id="e4a59-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4a59-129">Requirement</span></span> | <span data-ttu-id="e4a59-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e4a59-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a59-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4a59-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a59-132">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e4a59-132">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e4a59-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4a59-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a59-134">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e4a59-134">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e4a59-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4a59-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a59-136"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a59-136"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4a59-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4a59-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a59-138">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4a59-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e4a59-139">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="e4a59-139">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="e4a59-140">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="e4a59-140">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




