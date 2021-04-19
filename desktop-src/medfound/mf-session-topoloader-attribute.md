---
description: Contiene il CLSID di un caricatore della topologia per la sessione multimediale.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Attributo MF_SESSION_TOPOLOADER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318056"
---
# <a name="mf_session_topoloader-attribute"></a><span data-ttu-id="ccc8d-103">\_Attributo TOPOLOADER della sessione MF \_</span><span class="sxs-lookup"><span data-stu-id="ccc8d-103">MF\_SESSION\_TOPOLOADER attribute</span></span>

<span data-ttu-id="ccc8d-104">Contiene il CLSID di un caricatore della topologia per la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-104">Contains the CLSID of a topology loader for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="ccc8d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ccc8d-105">Data type</span></span>

<span data-ttu-id="ccc8d-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="ccc8d-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc8d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccc8d-107">Remarks</span></span>

<span data-ttu-id="ccc8d-108">È possibile usare questo attributo per fornire un caricatore di topologia personalizzato per la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-108">You can use this attribute to provide a custom topology loader for the Media Session.</span></span>

<span data-ttu-id="ccc8d-109">Impostare questo attributo utilizzando il parametro *pConfiguration* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o la funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="ccc8d-109">Set this attribute using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function or the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="ccc8d-110">Se questo attributo è impostato, la sessione multimediale chiama **CoCreateInstance** con il CLSID specificato quando crea il caricatore della topologia.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID when it creates the topology loader.</span></span> <span data-ttu-id="ccc8d-111">L'oggetto creato da questo CLSID deve esporre l'interfaccia [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="ccc8d-111">The object created by this CLSID must expose the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="ccc8d-112">Se questo attributo non è impostato, la sessione multimediale crea il caricatore della topologia predefinito fornito in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-112">If this attribute is not set, the Media Session creates the default topology loader provided in Media Foundation.</span></span>

<span data-ttu-id="ccc8d-113">Un caricatore di topologia deve supportare gli Apartment A thread multipli.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-113">A topology loader must support multithreaded apartments.</span></span> <span data-ttu-id="ccc8d-114">È necessario registrare il caricatore della topologia come ThreadingModel = "both".</span><span class="sxs-lookup"><span data-stu-id="ccc8d-114">You should register the topology loader as ThreadingModel="Both".</span></span> <span data-ttu-id="ccc8d-115">Inoltre, se si usa il caricatore della topologia all'interno del percorso multimediale protetto (PMP), il caricatore della topologia deve essere un componente attendibile.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-115">Also, if you are using the topology loader inside the protected media path (PMP), the topology loader must be a trusted component.</span></span> <span data-ttu-id="ccc8d-116">Per altre informazioni, vedere [percorso multimediale protetto](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="ccc8d-116">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

<span data-ttu-id="ccc8d-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ccc8d-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc8d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccc8d-118">Requirements</span></span>



| <span data-ttu-id="ccc8d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc8d-119">Requirement</span></span> | <span data-ttu-id="ccc8d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ccc8d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc8d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccc8d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc8d-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccc8d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ccc8d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccc8d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc8d-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccc8d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ccc8d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccc8d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc8d-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc8d-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc8d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccc8d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc8d-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ccc8d-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ccc8d-129">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="ccc8d-129">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="ccc8d-130">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="ccc8d-130">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="ccc8d-131">Attributi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="ccc8d-131">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="ccc8d-132">Caricatori topologia personalizzati</span><span class="sxs-lookup"><span data-stu-id="ccc8d-132">Custom Topology Loaders</span></span>](custom-topology-loaders.md)
</dt> </dl>

 

 




