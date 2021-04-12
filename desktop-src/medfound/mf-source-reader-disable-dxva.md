---
description: Specifica se il lettore di origine Abilita l'accelerazione video DirectX (DXVA) nel decodificatore video.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: Attributo MF_SOURCE_READER_DISABLE_DXVA (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348736"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a><span data-ttu-id="b45e4-103">MF \_ source \_ Reader \_ disabilitare l' \_ attributo DXVA</span><span class="sxs-lookup"><span data-stu-id="b45e4-103">MF\_SOURCE\_READER\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="b45e4-104">Specifica se il [lettore di origine](source-reader.md) Abilita l'accelerazione video DirectX (DXVA) nel decodificatore video.</span><span class="sxs-lookup"><span data-stu-id="b45e4-104">Specifies whether the [Source Reader](source-reader.md) enables DirectX Video Acceleration (DXVA) on the video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="b45e4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b45e4-105">Data type</span></span>

<span data-ttu-id="b45e4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b45e4-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b45e4-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b45e4-107">Get/set</span></span>

<span data-ttu-id="b45e4-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b45e4-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b45e4-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="b45e4-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b45e4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b45e4-110">Remarks</span></span>

<span data-ttu-id="b45e4-111">Questo attributo si applica se vengono soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b45e4-111">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="b45e4-112">Il lettore di origine decodifica un flusso video.</span><span class="sxs-lookup"><span data-stu-id="b45e4-112">The source reader decodes a video stream.</span></span>
-   <span data-ttu-id="b45e4-113">Il decodificatore video supporta la decodifica DXVA.</span><span class="sxs-lookup"><span data-stu-id="b45e4-113">The video decoder supports DXVA decoding.</span></span>
-   <span data-ttu-id="b45e4-114">L'applicazione usa l'attributo di [ \_ \_ \_ \_ gestione D3D del lettore di origine MF](mf-source-reader-d3d-manager.md) per impostare il [Gestione dispositivi Direct3D](direct3d-device-manager.md) nel lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="b45e4-114">The application uses the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute to set the [Direct3D Device Manager](direct3d-device-manager.md) on the source reader.</span></span>

<span data-ttu-id="b45e4-115">Questo attributo consente all'applicazione di disabilitare DXVA, pur continuando a eseguire la decodifica nelle superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b45e4-115">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="b45e4-116">Per impostazione predefinita, il lettore di origine usa il [Gestione dispositivi Direct3D](direct3d-device-manager.md) per due scopi:</span><span class="sxs-lookup"><span data-stu-id="b45e4-116">By default, the source reader uses the [Direct3D Device Manager](direct3d-device-manager.md) for two purposes:</span></span>

-   <span data-ttu-id="b45e4-117">Per abilitare la decodifica DXVA nel decodificatore video.</span><span class="sxs-lookup"><span data-stu-id="b45e4-117">To enable DXVA decoding in the video decoder.</span></span>
-   <span data-ttu-id="b45e4-118">Per allocare le superfici Direct3D per gli esempi video.</span><span class="sxs-lookup"><span data-stu-id="b45e4-118">To allocate Direct3D surfaces for the video samples.</span></span>

<span data-ttu-id="b45e4-119">Se il valore dell'attributo MF \_ source \_ Reader \_ Disable \_ DXVA è **true**, il lettore di origine Disabilita la decodifica DXVA, anche se usa ancora il [Gestione dispositivi Direct3D](direct3d-device-manager.md) per allocare le superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b45e4-119">If the value of the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is **TRUE**, the source reader does disables DXVA decoding, although it still uses the [Direct3D Device Manager](direct3d-device-manager.md) to allocate Direct3D surfaces.</span></span>

<span data-ttu-id="b45e4-120">Se l'attributo di [ \_ \_ \_ \_ gestione D3D di Reader Source Reader](mf-source-reader-d3d-manager.md) non è impostato, l'attributo MF \_ source \_ Reader \_ Disable \_ DXVA viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b45e4-120">If the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute is not set, the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is ignored.</span></span>

<span data-ttu-id="b45e4-121">Il valore predefinito di questo attributo è **false**, vale a dire che la decodifica DXVA è abilitata quando disponibile.</span><span class="sxs-lookup"><span data-stu-id="b45e4-121">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="b45e4-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b45e4-122">Requirements</span></span>



| <span data-ttu-id="b45e4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b45e4-123">Requirement</span></span> | <span data-ttu-id="b45e4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b45e4-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45e4-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b45e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b45e4-126">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b45e4-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b45e4-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b45e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b45e4-128">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b45e4-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b45e4-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b45e4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b45e4-130"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="b45e4-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b45e4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b45e4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b45e4-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b45e4-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b45e4-133">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="b45e4-133">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="b45e4-134">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="b45e4-134">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




