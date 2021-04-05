---
title: Messaggio di EM_GETSELTEXT (RichEdit. h)
description: Recupera il testo attualmente selezionato in un controllo Rich Edit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- Controlli di Windows Message EM_GETSELTEXT
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873714"
---
# <a name="em_getseltext-message"></a><span data-ttu-id="812b2-104">\_Messaggio GETSELTEXT em</span><span class="sxs-lookup"><span data-stu-id="812b2-104">EM\_GETSELTEXT message</span></span>

<span data-ttu-id="812b2-105">Recupera il testo attualmente selezionato in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="812b2-105">Retrieves the currently selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="812b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="812b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="812b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="812b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="812b2-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="812b2-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="812b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="812b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="812b2-110">Puntatore a un buffer che riceve il testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="812b2-110">Pointer to a buffer that receives the selected text.</span></span> <span data-ttu-id="812b2-111">L'applicazione chiamante deve garantire che il buffer sia sufficientemente grande da poter essere in possesso del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="812b2-111">The calling application must ensure that the buffer is large enough to hold the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="812b2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="812b2-112">Return value</span></span>

<span data-ttu-id="812b2-113">Questo messaggio restituisce il numero di caratteri copiati, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="812b2-113">This message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="812b2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="812b2-114">Requirements</span></span>



| <span data-ttu-id="812b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="812b2-115">Requirement</span></span> | <span data-ttu-id="812b2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="812b2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="812b2-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="812b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="812b2-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="812b2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="812b2-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="812b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="812b2-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="812b2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="812b2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="812b2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="812b2-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="812b2-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





