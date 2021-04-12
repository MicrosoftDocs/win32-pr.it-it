---
title: Messaggio EM_FILELINEINDEX (CommCtrl. h)
description: Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Controlli di Windows Message EM_FILELINEINDEX
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120135"
---
# <a name="em_filelineindex-message-commctrlh"></a><span data-ttu-id="fc7fa-104">Messaggio EM_FILELINEINDEX (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="fc7fa-104">EM_FILELINEINDEX message (CommCtrl.h)</span></span>

<span data-ttu-id="fc7fa-105">Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-105">Gets the character index of the first character of a specified line in a multiline edit control, independently of how lines are displayed on the screen..</span></span> <span data-ttu-id="fc7fa-106">Un indice dei caratteri è l'indice in base zero del carattere a partire dall'inizio del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc7fa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc7fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc7fa-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc7fa-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc7fa-109">Numero di riga in base zero.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-109">The zero-based line number.</span></span> <span data-ttu-id="fc7fa-110">Il valore-1 specifica il numero di riga corrente, ovvero la riga che contiene il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-110">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="fc7fa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc7fa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc7fa-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc7fa-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc7fa-113">Return value</span></span>

<span data-ttu-id="fc7fa-114">Il valore restituito è l'indice dei caratteri della riga specificata nel parametro *wParam* , indipendentemente dalla modalità di visualizzazione delle linee sullo schermo, oppure-1 se il numero di riga specificato è maggiore del numero di righe nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="fc7fa-114">The return value is the character index of the line specified in the *wParam* parameter, independently of how lines are displayed on the screen, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc7fa-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc7fa-115">Requirements</span></span>



| <span data-ttu-id="fc7fa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc7fa-116">Requirement</span></span> | <span data-ttu-id="fc7fa-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fc7fa-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7fa-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc7fa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7fa-119">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc7fa-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc7fa-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc7fa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7fa-121">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="fc7fa-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc7fa-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc7fa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc7fa-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc7fa-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc7fa-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc7fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7fa-125">**\_FILELINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="fc7fa-125">**EM\_FILELINEFROMCHAR**</span></span>](em-filelinefromchar.md)
</dt> </dl>

 

 





