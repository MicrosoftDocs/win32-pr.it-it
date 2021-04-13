---
title: Messaggio di EM_INSERTIMAGE (RichEdit. h)
description: Sostituisce la selezione con un BLOB che visualizza un'immagine.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- Controlli di Windows Message EM_INSERTIMAGE
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475557"
---
# <a name="em_insertimage-message"></a><span data-ttu-id="cc992-104">\_Messaggio INSERTIMAGE em</span><span class="sxs-lookup"><span data-stu-id="cc992-104">EM\_INSERTIMAGE message</span></span>

<span data-ttu-id="cc992-105">Sostituisce la selezione con un BLOB che visualizza un'immagine.</span><span class="sxs-lookup"><span data-stu-id="cc992-105">Replaces the selection with a blob that displays an image.</span></span>


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a><span data-ttu-id="cc992-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc992-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc992-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc992-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cc992-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cc992-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc992-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc992-110">Puntatore a una struttura [**di \_ \_ parametri dell'immagine RichEdit**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) che contiene il BLOB dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="cc992-110">A pointer to a [**RICHEDIT\_IMAGE\_PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) structure that contains the image blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc992-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc992-111">Return value</span></span>

<span data-ttu-id="cc992-112">Restituisce \_ OK se ha esito positivo o uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="cc992-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="cc992-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cc992-113">Return code</span></span>                                                                                    | <span data-ttu-id="cc992-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc992-114">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="cc992-115"><dt>**E \_ Non riuscita**</dt></span><span class="sxs-lookup"><span data-stu-id="cc992-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="cc992-116">Impossibile inserire l'immagine.</span><span class="sxs-lookup"><span data-stu-id="cc992-116">Cannot insert the image.</span></span> <br/>                          |
| <dl> <span data-ttu-id="cc992-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cc992-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="cc992-118">Il parametro *lParam* è null o punta a un'immagine non valida.</span><span class="sxs-lookup"><span data-stu-id="cc992-118">The *lParam* parameter is NULL or points to an invalid image.</span></span> |
| <dl> <span data-ttu-id="cc992-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cc992-119"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="cc992-120">La memoria disponibile è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="cc992-120">Insufficient memory is available.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="cc992-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc992-121">Remarks</span></span>

<span data-ttu-id="cc992-122">Se la selezione è un punto di inserimento, il BLOB dell'immagine viene inserito nel punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="cc992-122">If the selection is an insertion point, the image blob is inserted at the insertion point.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc992-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc992-123">Requirements</span></span>



| <span data-ttu-id="cc992-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc992-124">Requirement</span></span> | <span data-ttu-id="cc992-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cc992-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc992-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc992-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cc992-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cc992-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cc992-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc992-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cc992-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cc992-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc992-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc992-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc992-131"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc992-131"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc992-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc992-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc992-133">**\_INSERTTABLE em**</span><span class="sxs-lookup"><span data-stu-id="cc992-133">**EM\_INSERTTABLE**</span></span>](em-inserttable.md)
</dt> </dl>

 

 





