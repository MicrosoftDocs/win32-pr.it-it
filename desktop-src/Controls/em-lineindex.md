---
title: Messaggio EM_LINEINDEX (winuser. h)
description: Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Controlli di Windows Message EM_LINEINDEX
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964053"
---
# <a name="em_lineindex-message-winuserh"></a><span data-ttu-id="8534e-104">Messaggio EM_LINEINDEX (winuser. h)</span><span class="sxs-lookup"><span data-stu-id="8534e-104">EM_LINEINDEX message (Winuser.h)</span></span>

<span data-ttu-id="8534e-105">Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="8534e-105">Gets the character index of the first character of a specified line in a multiline edit control.</span></span> <span data-ttu-id="8534e-106">Un indice dei caratteri è l'indice in base zero del carattere a partire dall'inizio del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="8534e-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="8534e-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8534e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8534e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8534e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8534e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8534e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8534e-110">Numero di riga in base zero.</span><span class="sxs-lookup"><span data-stu-id="8534e-110">The zero-based line number.</span></span> <span data-ttu-id="8534e-111">Il valore-1 specifica il numero di riga corrente, ovvero la riga che contiene il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="8534e-111">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="8534e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8534e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8534e-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="8534e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8534e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8534e-114">Return value</span></span>

<span data-ttu-id="8534e-115">Il valore restituito è l'indice dei caratteri della riga specificata nel parametro *wParam* oppure è-1 se il numero di riga specificato è maggiore del numero di righe nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="8534e-115">The return value is the character index of the line specified in the *wParam* parameter, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8534e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8534e-116">Remarks</span></span>

<span data-ttu-id="8534e-117">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8534e-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8534e-118">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8534e-118">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8534e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8534e-119">Requirements</span></span>



| <span data-ttu-id="8534e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8534e-120">Requirement</span></span> | <span data-ttu-id="8534e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8534e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8534e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8534e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8534e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8534e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8534e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8534e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8534e-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8534e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8534e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8534e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8534e-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8534e-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8534e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8534e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8534e-129">**\_LINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="8534e-129">**EM\_LINEFROMCHAR**</span></span>](em-linefromchar.md)
</dt> </dl>

 

 





