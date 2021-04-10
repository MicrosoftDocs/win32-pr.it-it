---
title: Messaggio di EM_GETELLIPSISMODE (RichEdit. h)
description: Recupera la modalità corrente dei puntini di sospensione.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- Controlli di Windows Message EM_GETELLIPSISMODE
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119842"
---
# <a name="em_getellipsismode-message"></a><span data-ttu-id="54d5d-104">\_Messaggio GETELLIPSISMODE em</span><span class="sxs-lookup"><span data-stu-id="54d5d-104">EM\_GETELLIPSISMODE message</span></span>

<span data-ttu-id="54d5d-105">Recupera la modalità corrente dei puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="54d5d-105">Retrieves the current ellipsis mode.</span></span> <span data-ttu-id="54d5d-106">Quando è abilitata, viene visualizzato un pulsante con i puntini di sospensione () per il testo che non rientra nella finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="54d5d-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="54d5d-107">I puntini di sospensione vengono utilizzati solo quando il controllo non è attivo.</span><span class="sxs-lookup"><span data-stu-id="54d5d-107">The ellipsis is only used when the control is not active.</span></span> <span data-ttu-id="54d5d-108">Quando è attiva, le barre di scorrimento vengono usate per rivelare il testo che non rientra nella finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="54d5d-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a><span data-ttu-id="54d5d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="54d5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d5d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54d5d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54d5d-111">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="54d5d-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="54d5d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54d5d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54d5d-113">Puntatore a un valore DWORD che riceve uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="54d5d-113">Pointer to a DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="54d5d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="54d5d-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="54d5d-115">Significato</span><span class="sxs-lookup"><span data-stu-id="54d5d-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="54d5d-116"><dt>**PUNTIni di sospensione \_ nessuno**</dt></span><span class="sxs-lookup"><span data-stu-id="54d5d-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="54d5d-117">Non viene utilizzato alcun puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="54d5d-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="54d5d-118"><dt>**PUNTIni di sospensione \_**</dt></span><span class="sxs-lookup"><span data-stu-id="54d5d-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="54d5d-119">Puntini di sospensione alla fine (interruzioni forzate).</span><span class="sxs-lookup"><span data-stu-id="54d5d-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="54d5d-120"><dt>**parola con i PUNTIni di sospensione \_**</dt></span><span class="sxs-lookup"><span data-stu-id="54d5d-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="54d5d-121">Puntini di sospensione alla fine (Word Break).</span><span class="sxs-lookup"><span data-stu-id="54d5d-121">Ellipsis at the end (word break).</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d5d-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54d5d-122">Return value</span></span>

<span data-ttu-id="54d5d-123">Se wParam è 0 e lParam non è NULL, il valore restituito è uguale a TRUE; in caso contrario, il valore restituito è uguale a FALSE.</span><span class="sxs-lookup"><span data-stu-id="54d5d-123">If wparam is 0 and lparam is not NULL, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d5d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54d5d-124">Requirements</span></span>



| <span data-ttu-id="54d5d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="54d5d-125">Requirement</span></span> | <span data-ttu-id="54d5d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="54d5d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54d5d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54d5d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="54d5d-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="54d5d-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="54d5d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54d5d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="54d5d-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="54d5d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54d5d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54d5d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="54d5d-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="54d5d-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d5d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54d5d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d5d-134">**\_SETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="54d5d-134">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> <dt>

[<span data-ttu-id="54d5d-135">**\_GETELLIPSISSTATE em**</span><span class="sxs-lookup"><span data-stu-id="54d5d-135">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





