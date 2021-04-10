---
title: Messaggio di EM_GETTEXTRANGE (RichEdit. h)
description: Recupera un intervallo di caratteri specificato da un controllo Rich Edit.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- Controlli di Windows Message EM_GETTEXTRANGE
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964653"
---
# <a name="em_gettextrange-message"></a><span data-ttu-id="c7321-104">\_Messaggio GETTEXTRANGE em</span><span class="sxs-lookup"><span data-stu-id="c7321-104">EM\_GETTEXTRANGE message</span></span>

<span data-ttu-id="c7321-105">Recupera un intervallo di caratteri specificato da un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c7321-105">Retrieves a specified range of characters from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7321-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7321-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7321-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7321-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7321-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c7321-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c7321-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7321-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7321-110">Puntatore a una struttura [**TextRange**](/windows/win32/api/richedit/ns-richedit-textrangea) che specifica l'intervallo di caratteri da recuperare e un buffer in cui copiare i caratteri.</span><span class="sxs-lookup"><span data-stu-id="c7321-110">Pointer to a [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure that specifies the range of characters to retrieve and a buffer to copy the characters to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7321-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7321-111">Return value</span></span>

<span data-ttu-id="c7321-112">Il messaggio restituisce il numero di caratteri copiati, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c7321-112">The message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7321-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7321-113">Requirements</span></span>



| <span data-ttu-id="c7321-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7321-114">Requirement</span></span> | <span data-ttu-id="c7321-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c7321-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7321-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7321-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c7321-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7321-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7321-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7321-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c7321-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7321-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7321-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7321-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7321-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7321-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7321-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7321-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7321-123">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="c7321-123">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





