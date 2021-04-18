---
description: Fornisce un'interfaccia di callback per l'applicazione per ricevere un oggetto Enabler contenuto dalla sessione del percorso multimediale protetto (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Attributo MF_SESSION_CONTENT_PROTECTION_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315012"
---
# <a name="mf_session_content_protection_manager-attribute"></a><span data-ttu-id="7fe21-103">\_Attributo MF Session \_ Content \_ Protection \_ Manager</span><span class="sxs-lookup"><span data-stu-id="7fe21-103">MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="7fe21-104">Fornisce un'interfaccia di callback per l'applicazione per ricevere un oggetto Enabler contenuto dalla sessione del percorso multimediale protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="7fe21-104">Provides a callback interface for the application to receive a content enabler object from the protected media path (PMP) session.</span></span>

## <a name="data-type"></a><span data-ttu-id="7fe21-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7fe21-105">Data type</span></span>

<span data-ttu-id="7fe21-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="7fe21-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="7fe21-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fe21-107">Remarks</span></span>

<span data-ttu-id="7fe21-108">Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFContentProtectionManager* \*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fe21-108">The value of this attribute is a pointer to the application's [_ *IMFContentProtectionManager*\*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="7fe21-109">Impostare questo attributo nella sessione PMP utilizzando il parametro *pConfiguration* della funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="7fe21-109">Set this attribute on the PMP session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="7fe21-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7fe21-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe21-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fe21-111">Requirements</span></span>



| <span data-ttu-id="7fe21-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fe21-112">Requirement</span></span> | <span data-ttu-id="7fe21-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7fe21-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe21-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe21-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe21-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fe21-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7fe21-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe21-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe21-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7fe21-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7fe21-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fe21-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fe21-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe21-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe21-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fe21-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe21-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7fe21-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7fe21-122">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="7fe21-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="7fe21-123">**IMFAttributes:: Unknown**</span><span class="sxs-lookup"><span data-stu-id="7fe21-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="7fe21-124">Attributi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="7fe21-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="7fe21-125">Come riprodurre file multimediali protetti</span><span class="sxs-lookup"><span data-stu-id="7fe21-125">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




