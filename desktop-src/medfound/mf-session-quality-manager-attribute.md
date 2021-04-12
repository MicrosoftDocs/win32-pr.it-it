---
description: Contiene il CLSID di un gestore qualità per la sessione multimediale.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: Attributo MF_SESSION_QUALITY_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346656"
---
# <a name="mf_session_quality_manager-attribute"></a><span data-ttu-id="c526c-103">\_Attributo MF Session \_ Quality \_ Manager</span><span class="sxs-lookup"><span data-stu-id="c526c-103">MF\_SESSION\_QUALITY\_MANAGER attribute</span></span>

<span data-ttu-id="c526c-104">Contiene il CLSID di un gestore qualità per la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c526c-104">Contains the CLSID of a quality manager for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="c526c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c526c-105">Data type</span></span>

<span data-ttu-id="c526c-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="c526c-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="c526c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c526c-107">Remarks</span></span>

<span data-ttu-id="c526c-108">È possibile usare questo attributo per fornire un gestore di qualità personalizzato per la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c526c-108">You can use this attribute to provide a custom quality manager for the Media Session.</span></span>

<span data-ttu-id="c526c-109">Impostare questo attributo utilizzando il parametro *pConfiguration* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="c526c-109">Set this attribute by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="c526c-110">Se questo attributo è impostato, la sessione multimediale chiama **CoCreateInstance** con il CLSID specificato per creare il gestore qualità.</span><span class="sxs-lookup"><span data-stu-id="c526c-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID to create the quality manager.</span></span> <span data-ttu-id="c526c-111">L'oggetto creato da questo CLSID deve esporre l'interfaccia [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .</span><span class="sxs-lookup"><span data-stu-id="c526c-111">The object created by this CLSID must expose the [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) interface.</span></span>

<span data-ttu-id="c526c-112">Se questo attributo non è impostato, la sessione multimediale crea il gestore qualità predefinito fornito in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c526c-112">If this attribute is not set, the Media Session creates the default quality manager provided in Media Foundation.</span></span>

<span data-ttu-id="c526c-113">Se si vuole eseguire la sessione multimediale senza alcun gestore qualità, impostare questo attributo su **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="c526c-113">If you want to run the Media Session with no quality manager at all, set this attribute to **GUID\_NULL**.</span></span>

<span data-ttu-id="c526c-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c526c-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c526c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c526c-115">Requirements</span></span>



| <span data-ttu-id="c526c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c526c-116">Requirement</span></span> | <span data-ttu-id="c526c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c526c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c526c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c526c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c526c-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c526c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c526c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c526c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c526c-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c526c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c526c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c526c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c526c-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c526c-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c526c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c526c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c526c-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c526c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c526c-126">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="c526c-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="c526c-127">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="c526c-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="c526c-128">Attributi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="c526c-128">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




