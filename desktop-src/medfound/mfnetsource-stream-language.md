---
description: Archivia la stringa inviata nell'intestazione del Accept-Language.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: Proprietà MFNETSOURCE_STREAM_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401526"
---
# <a name="mfnetsource_stream_language-property"></a><span data-ttu-id="0f238-103">Proprietà della lingua del \_ flusso MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="0f238-103">MFNETSOURCE\_STREAM\_LANGUAGE property</span></span>

<span data-ttu-id="0f238-104">Archivia la stringa inviata nell'intestazione del Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="0f238-104">Stores the string sent in the Accept-Language header.</span></span>



<span data-ttu-id="0f238-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0f238-105">Data type</span></span>

<span data-ttu-id="0f238-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="0f238-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0f238-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="0f238-107">PROPVARIANT member</span></span>

<span data-ttu-id="0f238-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="0f238-108">\**WCHAR\** _</span></span>

<span data-ttu-id="0f238-109">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="0f238-109">VT\_LPWSTR</span></span>

<span data-ttu-id="0f238-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="0f238-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="0f238-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f238-111">Remarks</span></span>

<span data-ttu-id="0f238-112">La \_ costante del linguaggio del flusso MFNETSOURCE \_ definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0f238-112">The MFNETSOURCE\_STREAM\_LANGUAGE constant defines the GUID for the property key.</span></span> <span data-ttu-id="0f238-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="0f238-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="0f238-114">Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="0f238-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="0f238-115">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="0f238-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f238-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f238-116">Requirements</span></span>



| <span data-ttu-id="0f238-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f238-117">Requirement</span></span> | <span data-ttu-id="0f238-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0f238-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f238-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f238-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f238-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0f238-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0f238-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f238-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f238-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f238-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0f238-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f238-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f238-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f238-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f238-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f238-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f238-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f238-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0f238-127">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f238-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




