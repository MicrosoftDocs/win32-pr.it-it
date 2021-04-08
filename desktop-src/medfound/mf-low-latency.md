---
description: Abilita l'elaborazione a bassa latenza nella pipeline Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: Attributo MF_LOW_LATENCY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757865"
---
# <a name="mf_low_latency-attribute"></a><span data-ttu-id="51dee-103">\_Attributo MF low \_ latence</span><span class="sxs-lookup"><span data-stu-id="51dee-103">MF\_LOW\_LATENCY attribute</span></span>

<span data-ttu-id="51dee-104">Abilita l'elaborazione a bassa latenza nella pipeline Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="51dee-104">Enables low-latency processing in the Microsoft Media Foundation pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="51dee-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="51dee-105">Data type</span></span>

<span data-ttu-id="51dee-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51dee-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="51dee-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="51dee-107">Get/set</span></span>

<span data-ttu-id="51dee-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="51dee-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="51dee-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="51dee-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="51dee-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="51dee-110">Remarks</span></span>

<span data-ttu-id="51dee-111">La bassa latenza è definita come il minimo possibile ritardo da quando i dati multimediali vengono generati (o ricevuti) a quando viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="51dee-111">Low latency is defined as the smallest possible delay from when the media data is generated (or received) to when it is rendered.</span></span> <span data-ttu-id="51dee-112">Per gli scenari di comunicazione in tempo reale è consigliabile una bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="51dee-112">Low latency is desirable for real-time communication scenarios.</span></span> <span data-ttu-id="51dee-113">Per altri scenari, ad esempio la riproduzione o la transcodifica locale, in genere non è consigliabile abilitare la modalità a bassa latenza, in quanto può influire sulla qualità.</span><span class="sxs-lookup"><span data-stu-id="51dee-113">For other scenarios, such as local playback or transcoding, you typically should not enable low-latency mode, because it can affect quality.</span></span>

> [!Note]  
> <span data-ttu-id="51dee-114">Il valore GUID di questo attributo è identico alla proprietà [ \_ AVLowLatencyMode di codecapis](codecapi-avlowlatencymode.md) definita per l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="51dee-114">The GUID value of this attribute is identical to the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) property defined for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>

 

<span data-ttu-id="51dee-115">Impostare questo attributo sui componenti della pipeline come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="51dee-115">Set this attribute on pipeline components as follows:</span></span>

-   <span data-ttu-id="51dee-116">Origine supporto: usare il metodo [**IMFMediaSourceEx:: GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="51dee-116">Media source: Use the [**IMFMediaSourceEx::GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) method.</span></span>
-   <span data-ttu-id="51dee-117">Trasformazione Media Foundation (MFT): usare il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="51dee-117">Media Foundation transform (MFT): Use the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="51dee-118">Per i codificatori, il codificatore potrebbe supportare una bassa latenza tramite l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="51dee-118">For encoders, the encoder might support low latency through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
-   <span data-ttu-id="51dee-119">Sink multimediale: eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="51dee-119">Media sink: Query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="51dee-120">Le applicazioni in genere non impostano questo attributo direttamente sui componenti della pipeline, ma impostano invece l'attributo su uno degli oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="51dee-120">Applications typically do not set this attribute directly on the pipeline components, but instead set the attribute on one of the following objects:</span></span>

-   <span data-ttu-id="51dee-121">[Sessione multimediale](media-session.md): utilizzare il parametro *PConfiguation* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) oppure impostare l'attributo sulla topologia.</span><span class="sxs-lookup"><span data-stu-id="51dee-121">[Media Session](media-session.md): Use the *pConfiguation* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function, or else set the attribute on the topology.</span></span>
-   <span data-ttu-id="51dee-122">[Lettore di origine](source-reader.md): impostare l'attributo con le proprietà di configurazione quando si crea il lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="51dee-122">[Source Reader](source-reader.md): Set the attribute with the configuration properties when you create the Source Reader.</span></span> <span data-ttu-id="51dee-123">Per altre informazioni, vedere [attributi del lettore di origine](source-reader-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="51dee-123">For more information, see [Source Reader Attributes](source-reader-attributes.md).</span></span>
-   <span data-ttu-id="51dee-124">[Sink writer](sink-writer.md): impostare l'attributo con le proprietà di configurazione quando si crea il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="51dee-124">[Sink Writer](sink-writer.md): Set the attribute with the configuration properties when you create the Sink Writer.</span></span> <span data-ttu-id="51dee-125">Per altre informazioni, vedere [sink writer Attributes](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="51dee-125">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51dee-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51dee-126">Requirements</span></span>



| <span data-ttu-id="51dee-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="51dee-127">Requirement</span></span> | <span data-ttu-id="51dee-128">Valore</span><span class="sxs-lookup"><span data-stu-id="51dee-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51dee-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51dee-129">Minimum supported client</span></span><br/> | <span data-ttu-id="51dee-130">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="51dee-130">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="51dee-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51dee-131">Minimum supported server</span></span><br/> | <span data-ttu-id="51dee-132">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="51dee-132">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="51dee-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51dee-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="51dee-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="51dee-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51dee-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51dee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51dee-136">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51dee-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="51dee-137">Attributi del writer di sink</span><span class="sxs-lookup"><span data-stu-id="51dee-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="51dee-138">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="51dee-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> <dt>

[<span data-ttu-id="51dee-139">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="51dee-139">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
