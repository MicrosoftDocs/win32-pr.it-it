---
description: Contiene un puntatore al Gestione dispositivi DXGI per il writer del sink.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Attributo MF_SINK_WRITER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318053"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a><span data-ttu-id="1ee16-103">\_ \_ \_ Attributo gestione D3D del writer di sink MF \_</span><span class="sxs-lookup"><span data-stu-id="1ee16-103">MF\_SINK\_WRITER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="1ee16-104">Contiene un puntatore al Gestione dispositivi DXGI per il [writer del sink](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="1ee16-104">Contains a pointer to the DXGI Device Manager for the [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="1ee16-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1ee16-105">Data type</span></span>

<span data-ttu-id="1ee16-106">**IMFDXGIDeviceManager \** _ archiviato come _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="1ee16-106">**IMFDXGIDeviceManager\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="remarks"></a><span data-ttu-id="1ee16-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ee16-107">Remarks</span></span>

<span data-ttu-id="1ee16-108">Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="1ee16-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="1ee16-109">Usare questo attributo per fornire un dispositivo Direct3D per tutti i codificatori video o i sink di supporto caricati dal writer del sink.</span><span class="sxs-lookup"><span data-stu-id="1ee16-109">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the Sink Writer.</span></span>

<span data-ttu-id="1ee16-110">Utilizzare questo attributo con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ee16-110">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="1ee16-111">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="1ee16-111">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="1ee16-112">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="1ee16-112">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="1ee16-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ee16-113">Requirements</span></span>



| <span data-ttu-id="1ee16-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee16-114">Requirement</span></span> | <span data-ttu-id="1ee16-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1ee16-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee16-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ee16-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee16-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1ee16-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="1ee16-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ee16-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee16-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1ee16-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1ee16-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ee16-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee16-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ee16-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee16-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ee16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee16-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ee16-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ee16-124">Writer sink</span><span class="sxs-lookup"><span data-stu-id="1ee16-124">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 




