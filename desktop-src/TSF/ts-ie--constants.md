---
title: Costanti TS_IE_ (Textstor. h)
description: Le \_ costanti IE \_ \ ts \ descrivono come inserire testo che può contenere oggetti incorporati utilizzati da servizi di testo.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119387"
---
# <a name="ts_ie_-constants"></a><span data-ttu-id="229ee-103">\_Costanti di IE di Servizi terminal \_ \*</span><span class="sxs-lookup"><span data-stu-id="229ee-103">TS\_IE\_\* Constants</span></span>

<span data-ttu-id="229ee-104">Le \_ \_ \* costanti di IE TS descrivono come inserire testo che può contenere oggetti incorporati utilizzati da servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="229ee-104">The TS\_IE\_\* constants describe how to insert text that can contain embedded objects used by text services.</span></span>



| <span data-ttu-id="229ee-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="229ee-105">Constant/value</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="229ee-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="229ee-106">Description</span></span>                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <span data-ttu-id="229ee-107"><dt>**Servizi terminal \_ \_Correzione di IE**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="229ee-107"><dt>**TS\_IE\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>    | <span data-ttu-id="229ee-108">Il testo è una trasformazione (correzione) del contenuto esistente e vengono mantenute le informazioni di markup di testo (metadati) speciali, ad esempio i dati del file WAV o un identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="229ee-108">The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier.</span></span><br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <span data-ttu-id="229ee-109"><dt>**Servizi terminal \_ \_Composizione IE**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="229ee-109"><dt>**TS\_IE\_COMPOSITION**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="229ee-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="229ee-110">Not used.</span></span><br/>                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="229ee-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="229ee-111">Remarks</span></span>

<span data-ttu-id="229ee-112">Queste costanti vengono usate nel parametro *dwFlags* di [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) e [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="229ee-112">These constants are used in the *dwFlags* parameter of [ITextStoreACP::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) and [ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).</span></span>

## <a name="requirements"></a><span data-ttu-id="229ee-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="229ee-113">Requirements</span></span>



| <span data-ttu-id="229ee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="229ee-114">Requirement</span></span> | <span data-ttu-id="229ee-115">Valore</span><span class="sxs-lookup"><span data-stu-id="229ee-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="229ee-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="229ee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="229ee-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="229ee-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="229ee-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="229ee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="229ee-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="229ee-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="229ee-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="229ee-120">Redistributable</span></span><br/>          | <span data-ttu-id="229ee-121">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="229ee-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="229ee-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="229ee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="229ee-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="229ee-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="229ee-124">IDL</span><span class="sxs-lookup"><span data-stu-id="229ee-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="229ee-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="229ee-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229ee-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="229ee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229ee-127">ITextStoreACP:: InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="229ee-127">ITextStoreACP::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[<span data-ttu-id="229ee-128">ITextStoreAnchor::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="229ee-128">ITextStoreAnchor::InsertEmbedded</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





