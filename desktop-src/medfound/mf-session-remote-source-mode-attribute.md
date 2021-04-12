---
description: Specifica che l'origine del supporto verrà creata in un processo remoto.
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: Attributo MF_SESSION_REMOTE_SOURCE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232529"
---
# <a name="mf_session_remote_source_mode-attribute"></a><span data-ttu-id="86feb-103">\_ \_ \_ Attributo modalità origine remota della sessione MF \_</span><span class="sxs-lookup"><span data-stu-id="86feb-103">MF\_SESSION\_REMOTE\_SOURCE\_MODE attribute</span></span>

<span data-ttu-id="86feb-104">Specifica che l'origine del supporto verrà creata in un processo remoto.</span><span class="sxs-lookup"><span data-stu-id="86feb-104">Specifies that the media source will be created in a remote process.</span></span>

## <a name="data-type"></a><span data-ttu-id="86feb-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="86feb-105">Data type</span></span>

<span data-ttu-id="86feb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="86feb-106">**UINT32**</span></span>

<span data-ttu-id="86feb-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="86feb-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86feb-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="86feb-108">Remarks</span></span>

<span data-ttu-id="86feb-109">È possibile impostare questo attributo sulla sessione del percorso multimediale protetto (PMP) utilizzando il parametro *pConfiguration* della funzione [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="86feb-109">You can set this attribute on the protected media path (PMP) session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="86feb-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="86feb-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="86feb-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86feb-111">Requirements</span></span>



| <span data-ttu-id="86feb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="86feb-112">Requirement</span></span> | <span data-ttu-id="86feb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="86feb-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86feb-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86feb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="86feb-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86feb-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="86feb-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86feb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="86feb-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86feb-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="86feb-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86feb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="86feb-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86feb-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86feb-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86feb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86feb-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86feb-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="86feb-122">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="86feb-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="86feb-123">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="86feb-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="86feb-124">Attributi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="86feb-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="86feb-125">Sessione multimediale PMP</span><span class="sxs-lookup"><span data-stu-id="86feb-125">PMP Media Session</span></span>](pmp-media-session.md)
</dt> </dl>

 

 




