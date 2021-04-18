---
title: Costanti TF_IAS_ (msctf. h)
description: Le \_ costanti TF IAS \_ \ vengono usate come flag bit nei metodi che inseriscono testo o oggetti incorporati a una selezione o a un punto di inserimento.
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301568"
---
# <a name="tf_ias_-constants"></a><span data-ttu-id="b6413-103">\_Costanti IAS \_ \* TF</span><span class="sxs-lookup"><span data-stu-id="b6413-103">TF\_IAS\_\* Constants</span></span>

<span data-ttu-id="b6413-104">Le \_ costanti TF IAS \_ \* vengono usate come flag bit nei metodi che inseriscono testo o oggetti incorporati in una selezione o in un punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="b6413-104">The TF\_IAS\_\* constants are used as bitfield flags in methods that insert text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="b6413-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b6413-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="b6413-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6413-106">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <span data-ttu-id="b6413-107"><dt>**Tf \_ IAS \_ noquery**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b6413-107"><dt>**TF\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                       | <span data-ttu-id="b6413-108">Il testo viene inserito e il puntatore di intervallo è impostato su **null** all'uscita.</span><span class="sxs-lookup"><span data-stu-id="b6413-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="b6413-109">Non può essere combinato con il \_ flag QUERYONLY di TF IAS \_ .</span><span class="sxs-lookup"><span data-stu-id="b6413-109">Cannot be combined with the TF\_IAS\_QUERYONLY flag.</span></span><br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <span data-ttu-id="b6413-110"><dt>**Tf \_ IAS \_ QUERYONLY**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="b6413-110"><dt>**TF\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                 | <span data-ttu-id="b6413-111">Non eseguire l'istruzione INSERT.</span><span class="sxs-lookup"><span data-stu-id="b6413-111">Do not perform the insert.</span></span> <span data-ttu-id="b6413-112">Il chiamante richiede l'impostazione del puntatore di intervallo.</span><span class="sxs-lookup"><span data-stu-id="b6413-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="b6413-113">Non può essere combinato con il \_ \_ flag noquery di TF IAS.</span><span class="sxs-lookup"><span data-stu-id="b6413-113">Cannot be combined with the TF\_IAS\_NOQUERY flag.</span></span><br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <span data-ttu-id="b6413-114"><dt>**Tf \_ IAS \_ Nessuna \_ \_ composizione predefinita**</dt> <dt>(0x80000000)</dt></span><span class="sxs-lookup"><span data-stu-id="b6413-114"><dt>**TF\_IAS\_NO\_DEFAULT\_COMPOSITION**</dt> <dt>( 0x80000000 )</dt></span></span> </dl> | <span data-ttu-id="b6413-115">TSF non creerà una composizione predefinita se è necessaria una composizione.</span><span class="sxs-lookup"><span data-stu-id="b6413-115">TSF will not create a default composition if a composition is required.</span></span> <span data-ttu-id="b6413-116">Il chiamante deve avviare una composizione sull'intervallo.</span><span class="sxs-lookup"><span data-stu-id="b6413-116">Caller must start a composition over the range.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="b6413-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6413-117">Requirements</span></span>



| <span data-ttu-id="b6413-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6413-118">Requirement</span></span> | <span data-ttu-id="b6413-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b6413-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6413-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6413-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6413-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6413-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b6413-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6413-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6413-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6413-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6413-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b6413-124">Redistributable</span></span><br/>          | <span data-ttu-id="b6413-125">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b6413-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="b6413-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6413-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6413-127"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6413-127"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6413-128">IDL</span><span class="sxs-lookup"><span data-stu-id="b6413-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6413-129"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6413-129"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6413-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6413-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6413-131">ITextStoreACP:: InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="b6413-131">ITextStoreACP::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="b6413-132">ITextStoreACP:: InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="b6413-132">ITextStoreACP::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="b6413-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="b6413-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="b6413-134">ITextStoreAnchor::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="b6413-134">ITextStoreAnchor::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="b6413-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span><span class="sxs-lookup"><span data-stu-id="b6413-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="b6413-136">ITfInsertAtSelection::InsertTextAtSelection</span><span class="sxs-lookup"><span data-stu-id="b6413-136">ITfInsertAtSelection::InsertTextAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





