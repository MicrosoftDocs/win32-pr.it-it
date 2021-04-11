---
title: Costanti TF_SD_ (msctf. h)
description: Le \_ costanti TF SD \_ \ descrivono lo stato del documento.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119119"
---
# <a name="tf_sd_-constants"></a><span data-ttu-id="1be6b-103">\_Costanti SD \_ \* TF</span><span class="sxs-lookup"><span data-stu-id="1be6b-103">TF\_SD\_\* Constants</span></span>

<span data-ttu-id="1be6b-104">Le \_ costanti SD TF \_ \* descrivono lo stato del documento.</span><span class="sxs-lookup"><span data-stu-id="1be6b-104">The TF\_SD\_\* constants describe the document status.</span></span>



| <span data-ttu-id="1be6b-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="1be6b-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="1be6b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1be6b-106">Description</span></span>                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <span data-ttu-id="1be6b-107"><dt>**Tf \_ SD \_ ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt></span><span class="sxs-lookup"><span data-stu-id="1be6b-107"><dt>**TF\_SD\_READONLY**</dt> <dt>( TS\_SD\_READONLY )</dt></span></span> </dl> | <span data-ttu-id="1be6b-108">Il documento è di sola lettura e non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="1be6b-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <span data-ttu-id="1be6b-109"><dt>**Tf \_ \_caricamento SD**</dt> <dt>( \_ caricamento SD TS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="1be6b-109"><dt>**TF\_SD\_LOADING**</dt> <dt>( TS\_SD\_LOADING )</dt></span></span> </dl>     | <span data-ttu-id="1be6b-110">Il documento viene caricato e può essere incompleto.</span><span class="sxs-lookup"><span data-stu-id="1be6b-110">The document is loading and can be incomplete.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="1be6b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1be6b-111">Remarks</span></span>

<span data-ttu-id="1be6b-112">Il membro **dwDynamicFlags** della struttura [di \_ stato TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) usa queste costanti.</span><span class="sxs-lookup"><span data-stu-id="1be6b-112">The **dwDynamicFlags** member of the [TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="1be6b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1be6b-113">Requirements</span></span>



| <span data-ttu-id="1be6b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1be6b-114">Requirement</span></span> | <span data-ttu-id="1be6b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1be6b-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1be6b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1be6b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1be6b-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1be6b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1be6b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1be6b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1be6b-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1be6b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1be6b-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1be6b-120">Redistributable</span></span><br/>          | <span data-ttu-id="1be6b-121">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1be6b-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="1be6b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1be6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be6b-123"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="1be6b-123"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="1be6b-124">IDL</span><span class="sxs-lookup"><span data-stu-id="1be6b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1be6b-125"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1be6b-125"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be6b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1be6b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1be6b-127">[\_stato TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1be6b-127">[TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1be6b-128">\_Costanti SD \_ \* TS</span><span class="sxs-lookup"><span data-stu-id="1be6b-128">TS\_SD\_\* Constants</span></span>](ts-sd--constants.md)
</dt> <dt>

[<span data-ttu-id="1be6b-129">ITfContextOwner:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="1be6b-129">ITfContextOwner::GetStatus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[<span data-ttu-id="1be6b-130">ITfContextOwnerServices:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="1be6b-130">ITfContextOwnerServices::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[<span data-ttu-id="1be6b-131">ITextStoreACP:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="1be6b-131">ITextStoreACP::GetStatus</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[<span data-ttu-id="1be6b-132">ITfStatusSunk:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="1be6b-132">ITfStatusSunk::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

