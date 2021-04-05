---
title: TS_ATTRID (Textstor. h)
description: Il \_ tipo di dati ATTRID di Servizi terminal viene usato per identificare un attributo di testo.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739783"
---
# <a name="ts_attrid"></a><span data-ttu-id="d4ba2-104">ATTRID di Servizi terminal \_</span><span class="sxs-lookup"><span data-stu-id="d4ba2-104">TS\_ATTRID</span></span>

<span data-ttu-id="d4ba2-105">Il tipo di dati **\_ ATTRID di Servizi terminal** viene usato per identificare un attributo di testo.</span><span class="sxs-lookup"><span data-stu-id="d4ba2-105">The **TS\_ATTRID** data type is used to identify a text attribute.</span></span>


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a><span data-ttu-id="d4ba2-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4ba2-106">Remarks</span></span>

<span data-ttu-id="d4ba2-107">Un elenco di GUID predefiniti per ATTRID di Servizi terminal \_ è in tsattrs. h.</span><span class="sxs-lookup"><span data-stu-id="d4ba2-107">A list of predefined GUIDs for TS\_ATTRID is in tsattrs.h.</span></span>

<span data-ttu-id="d4ba2-108">I GUID TSATTRID \_ Text \_ VERTICALWRITING e TSATTRID \_ Text \_ Orientation sono utili per le applicazioni che devono corrispondere al testo di input da correggere.</span><span class="sxs-lookup"><span data-stu-id="d4ba2-108">The GUIDs TSATTRID\_Text\_VerticalWriting and TSATTRID\_Text\_Orientation are useful for applications to match input text that is to be corrected.</span></span> <span data-ttu-id="d4ba2-109">È possibile creare GUID aggiuntivi definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d4ba2-109">Additional user-defined GUIDs can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ba2-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4ba2-110">Requirements</span></span>



| <span data-ttu-id="d4ba2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4ba2-111">Requirement</span></span> | <span data-ttu-id="d4ba2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d4ba2-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ba2-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4ba2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ba2-114">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="d4ba2-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="d4ba2-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4ba2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ba2-116">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d4ba2-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="d4ba2-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d4ba2-117">Redistributable</span></span><br/>          | <span data-ttu-id="d4ba2-118">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d4ba2-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="d4ba2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4ba2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ba2-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ba2-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4ba2-121">IDL</span><span class="sxs-lookup"><span data-stu-id="d4ba2-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4ba2-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4ba2-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ba2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4ba2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ba2-124">**ITextStoreACP:: FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-124">**ITextStoreACP::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="d4ba2-125">**ITextStoreACP:: RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-125">**ITextStoreACP::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="d4ba2-126">**ITextStoreACP:: RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-126">**ITextStoreACP::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="d4ba2-127">**ITextStoreACP:: RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-127">**ITextStoreACP::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="d4ba2-128">**ITextStoreACPSink:: OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-128">**ITextStoreACPSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="d4ba2-129">**ITextStoreAnchor::FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-129">**ITextStoreAnchor::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="d4ba2-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="d4ba2-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="d4ba2-132">**ITextStoreAnchor::RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-132">**ITextStoreAnchor::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="d4ba2-133">**ITextStoreAnchorSink::OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-133">**ITextStoreAnchorSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="d4ba2-134">**ATTRVAL di Servizi terminal \_**</span><span class="sxs-lookup"><span data-stu-id="d4ba2-134">**TS\_ATTRVAL**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





