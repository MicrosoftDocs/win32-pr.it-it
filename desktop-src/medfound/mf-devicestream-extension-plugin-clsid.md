---
description: Specifica il CLSID di un plug-in di post-elaborazione per un dispositivo di acquisizione video.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: Attributo MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307976"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a><span data-ttu-id="553a7-103">\_ \_ \_ Attributo CLSID del plug \_ -in dell'estensione MF DEVICESTREAM</span><span class="sxs-lookup"><span data-stu-id="553a7-103">MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute</span></span>

<span data-ttu-id="553a7-104">Specifica il CLSID di un plug-in di post-elaborazione per un dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="553a7-104">Specifies the CLSID of a post-processing plug-in for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="553a7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="553a7-105">Data type</span></span>

<span data-ttu-id="553a7-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="553a7-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="553a7-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="553a7-107">Remarks</span></span>

<span data-ttu-id="553a7-108">Un plug-in di post-elaborazione è un MFT che elabora l'immagine video dopo che è stata acquisita.</span><span class="sxs-lookup"><span data-stu-id="553a7-108">A post-processing plug-in is an MFT that processes the video image after it is captured.</span></span> <span data-ttu-id="553a7-109">Il fornitore dell'hardware può includere un plug-in di post-elaborazione come parte del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="553a7-109">The hardware vendor can include a post-processing plug-in as part of the installation package.</span></span> <span data-ttu-id="553a7-110">In tal caso, l'origine di acquisizione video imposta \_ l' \_ \_ attributo CLSID del plug-in dell'estensione MF DEVICESTREAM sul \_ CLSID del plug-in.</span><span class="sxs-lookup"><span data-stu-id="553a7-110">If so, the video capture source sets the MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute to the CLSID of the plug-in.</span></span>

<span data-ttu-id="553a7-111">Per ottenere questo attributo, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="553a7-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="553a7-112">Eseguire una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="553a7-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="553a7-113">Chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.</span><span class="sxs-lookup"><span data-stu-id="553a7-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="553a7-114">Chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) per ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="553a7-114">Call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) to get the attribute.</span></span>

<span data-ttu-id="553a7-115">Per creare il plug-in, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="553a7-115">To create the plug-in, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="requirements"></a><span data-ttu-id="553a7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="553a7-116">Requirements</span></span>



| <span data-ttu-id="553a7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="553a7-117">Requirement</span></span> | <span data-ttu-id="553a7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="553a7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="553a7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="553a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="553a7-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="553a7-120">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="553a7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="553a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="553a7-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="553a7-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="553a7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="553a7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="553a7-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="553a7-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="553a7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="553a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553a7-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="553a7-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
