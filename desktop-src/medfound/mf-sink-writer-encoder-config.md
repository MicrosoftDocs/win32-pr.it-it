---
description: Contiene un puntatore a un archivio di proprietà con proprietà di codifica.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Attributo MF_SINK_WRITER_ENCODER_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757400"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a><span data-ttu-id="e3ef2-103">\_Attributo di \_ \_ configurazione del codificatore MF sink writer \_</span><span class="sxs-lookup"><span data-stu-id="e3ef2-103">MF\_SINK\_WRITER\_ENCODER\_CONFIG attribute</span></span>

<span data-ttu-id="e3ef2-104">Contiene un puntatore a un archivio di proprietà con proprietà di codifica.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-104">Contains a pointer to a property store with encoding properties.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3ef2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e3ef2-105">Data type</span></span>

<span data-ttu-id="e3ef2-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="e3ef2-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="e3ef2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3ef2-107">Remarks</span></span>

<span data-ttu-id="e3ef2-108">Il valore di questo attributo è un puntatore [_ *IPropertyStore* \*](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="e3ef2-108">The value of this attribute is an [_ *IPropertyStore*\*](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer.</span></span>

<span data-ttu-id="e3ef2-109">Questo attributo consente a un'applicazione di impostare le proprietà di codifica quando si utilizza il [writer del sink](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="e3ef2-109">This attribute enables an application to set encoding properties when using the [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="e3ef2-110">Per impostare questo attributo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="e3ef2-110">To set this attribute, perform the following steps:</span></span>

1.  <span data-ttu-id="e3ef2-111">Chiamare [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) per creare un nuovo archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-111">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a new property store.</span></span>
2.  <span data-ttu-id="e3ef2-112">Impostare le proprietà del codificatore nell'archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-112">Set encoder properties on the property store.</span></span> <span data-ttu-id="e3ef2-113">Le proprietà disponibili dipendono dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-113">The available properties depends on the encoder.</span></span> <span data-ttu-id="e3ef2-114">Per altre informazioni, vedere [oggetti codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="e3ef2-114">For more information, see [Codec Objects](codecobjects.md).</span></span>
3.  <span data-ttu-id="e3ef2-115">Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-115">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
4.  <span data-ttu-id="e3ef2-116">Chiamare [**IMFAttributes:: Unknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) per impostare il puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) nell'archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-116">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer on the attribute store.</span></span>
5.  <span data-ttu-id="e3ef2-117">Crea una nuova istanza del writer del sink.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-117">Create a new instance of the Sink Writer.</span></span> <span data-ttu-id="e3ef2-118">Passare il puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) alla funzione di creazione.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-118">Pass the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer to the creation function.</span></span> <span data-ttu-id="e3ef2-119">Per altre informazioni, vedere [sink writer Attributes](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e3ef2-119">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

<span data-ttu-id="e3ef2-120">Il writer di sink imposta le proprietà del codificatore prima di impostare i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="e3ef2-120">The Sink Writer sets the properties on the encoder before setting the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ef2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3ef2-121">Requirements</span></span>



| <span data-ttu-id="e3ef2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3ef2-122">Requirement</span></span> | <span data-ttu-id="e3ef2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e3ef2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ef2-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3ef2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ef2-125">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e3ef2-125">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e3ef2-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3ef2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ef2-127">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="e3ef2-127">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e3ef2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3ef2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3ef2-129"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3ef2-129"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ef2-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3ef2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ef2-131">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3ef2-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3ef2-132">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="e3ef2-132">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="e3ef2-133">Attributi del writer di sink</span><span class="sxs-lookup"><span data-stu-id="e3ef2-133">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 
