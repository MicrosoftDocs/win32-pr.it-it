---
title: Costanti TS_LF_ (Textstor. h)
description: Il \_ \_ tipo di blocco del documento è specificato nelle costanti di Servizi terminal.
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300942"
---
# <a name="ts_lf_-constants"></a><span data-ttu-id="13806-103">Costanti di TS \_ LF \_ \*</span><span class="sxs-lookup"><span data-stu-id="13806-103">TS\_LF\_\* Constants</span></span>

<span data-ttu-id="13806-104">Le \_ \_ \* costanti di TS LF specificano il tipo di blocco del documento.</span><span class="sxs-lookup"><span data-stu-id="13806-104">The TS\_LF\_\* constants specify the type of document lock.</span></span>



| <span data-ttu-id="13806-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="13806-105">Constant/value</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="13806-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13806-106">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <span data-ttu-id="13806-107"><dt>**Servizi terminal \_ \_Sincronizzazione LF**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="13806-107"><dt>**TS\_LF\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                | <span data-ttu-id="13806-108">Il documento ha un blocco sincrono se questo flag è combinato con altri flag.</span><span class="sxs-lookup"><span data-stu-id="13806-108">The document has a synchronous-lock if this flag is combined with other flags.</span></span><br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <span data-ttu-id="13806-109"><dt>**Servizi terminal \_ \_Lettura LF**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="13806-109"><dt>**TS\_LF\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                | <span data-ttu-id="13806-110">Il documento ha un blocco di sola lettura e non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="13806-110">The document has a read-only lock and cannot be modified.</span></span><br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <span data-ttu-id="13806-111"><dt>**Servizi terminal \_ LF \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="13806-111"><dt>**TS\_LF\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl> | <span data-ttu-id="13806-112">Il documento ha un blocco di lettura/scrittura e può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="13806-112">The document has a read/write lock and can be modified.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="13806-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13806-113">Requirements</span></span>



| <span data-ttu-id="13806-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="13806-114">Requirement</span></span> | <span data-ttu-id="13806-115">Valore</span><span class="sxs-lookup"><span data-stu-id="13806-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13806-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13806-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13806-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13806-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="13806-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13806-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13806-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13806-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13806-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="13806-120">Redistributable</span></span><br/>          | <span data-ttu-id="13806-121">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13806-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="13806-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13806-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="13806-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="13806-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="13806-124">IDL</span><span class="sxs-lookup"><span data-stu-id="13806-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13806-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13806-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13806-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13806-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13806-127">Blocchi del documento</span><span class="sxs-lookup"><span data-stu-id="13806-127">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="13806-128">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="13806-128">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="13806-129">ITextStoreACPSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="13806-129">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="13806-130">ITextStoreAnchor:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="13806-130">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="13806-131">ITextStoreAnchorSink:: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="13806-131">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





