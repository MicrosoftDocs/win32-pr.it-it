---
title: Messaggio di EM_SETELLIPSISMODE (RichEdit. h)
description: Questo messaggio consente di impostare la modalità corrente dei puntini di sospensione.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- Controlli di Windows Message EM_SETELLIPSISMODE
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048654"
---
# <a name="em_setellipsismode-message"></a><span data-ttu-id="27a2b-104">\_Messaggio SETELLIPSISMODE em</span><span class="sxs-lookup"><span data-stu-id="27a2b-104">EM\_SETELLIPSISMODE message</span></span>

<span data-ttu-id="27a2b-105">Questo messaggio consente di impostare la modalità corrente dei puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="27a2b-105">This message sets the current ellipsis mode.</span></span> <span data-ttu-id="27a2b-106">Quando è abilitata, viene visualizzato un pulsante con i puntini di sospensione () per il testo che non rientra nella finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="27a2b-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="27a2b-107">I puntini di sospensione vengono utilizzati solo quando il controllo non è attivo.</span><span class="sxs-lookup"><span data-stu-id="27a2b-107">The ellipsis is only used when the control isn t active.</span></span> <span data-ttu-id="27a2b-108">Quando è attiva, le barre di scorrimento vengono usate per rivelare il testo che non rientra nella finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="27a2b-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a><span data-ttu-id="27a2b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="27a2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27a2b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27a2b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27a2b-111">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="27a2b-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="27a2b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27a2b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27a2b-113">Valore DWORD che riceve uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="27a2b-113">A DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="27a2b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="27a2b-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="27a2b-115">Significato</span><span class="sxs-lookup"><span data-stu-id="27a2b-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="27a2b-116"><dt>**PUNTIni di sospensione \_ nessuno**</dt></span><span class="sxs-lookup"><span data-stu-id="27a2b-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="27a2b-117">Non viene utilizzato alcun puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="27a2b-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="27a2b-118"><dt>**PUNTIni di sospensione \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27a2b-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="27a2b-119">Puntini di sospensione alla fine (interruzioni forzate).</span><span class="sxs-lookup"><span data-stu-id="27a2b-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="27a2b-120"><dt>**parola con i PUNTIni di sospensione \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27a2b-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="27a2b-121">Puntini di sospensione alla fine (Word Break).</span><span class="sxs-lookup"><span data-stu-id="27a2b-121">Ellipsis at the end (word break).</span></span><br/>   |



 

<span data-ttu-id="27a2b-122">Tutti i bit per questi valori si adattano **alla \_ maschera dei puntini** di sospensione.</span><span class="sxs-lookup"><span data-stu-id="27a2b-122">The bits for these values all fit in the **ELLIPSIS\_MASK**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27a2b-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27a2b-123">Return value</span></span>

<span data-ttu-id="27a2b-124">Se wParam è 0 e lParam è uno dei valori nella tabella precedente, il valore restituito è uguale a TRUE; in caso contrario, il valore restituito è uguale a FALSE.</span><span class="sxs-lookup"><span data-stu-id="27a2b-124">If wparam is 0 and lparam is one of the values in the table above, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="27a2b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27a2b-125">Requirements</span></span>



| <span data-ttu-id="27a2b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="27a2b-126">Requirement</span></span> | <span data-ttu-id="27a2b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="27a2b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27a2b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27a2b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="27a2b-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="27a2b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="27a2b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27a2b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="27a2b-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="27a2b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27a2b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27a2b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="27a2b-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27a2b-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27a2b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27a2b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a2b-135">**\_GETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="27a2b-135">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="27a2b-136">**\_GETELLIPSISSTATE em**</span><span class="sxs-lookup"><span data-stu-id="27a2b-136">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





