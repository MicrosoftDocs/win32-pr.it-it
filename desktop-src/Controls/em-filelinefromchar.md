---
title: Messaggio EM_FILELINEFROMCHAR (CommCtrl. h)
description: Ottiene l'indice della riga che contiene l'indice del carattere specificato in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Controlli di Windows Message EM_FILELINEFROMCHAR
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477332"
---
# <a name="em_filelinefromchar-message"></a><span data-ttu-id="96d86-104">\_Messaggio FILELINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="96d86-104">EM\_FILELINEFROMCHAR message</span></span>

<span data-ttu-id="96d86-105">Ottiene l'indice della riga che contiene l'indice del carattere specificato in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="96d86-105">Gets the index of the line that contains the specified character index in a multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="96d86-106">Un indice dei caratteri è l'indice in base zero del carattere a partire dall'inizio del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="96d86-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="96d86-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="96d86-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d86-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96d86-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96d86-109">Indice dei caratteri del carattere contenuto nella riga di cui è necessario recuperare il numero.</span><span class="sxs-lookup"><span data-stu-id="96d86-109">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="96d86-110">Se questo parametro è-1, **em \_ FILELINEFROMCHAR** Recupera il numero di riga della riga corrente (la riga contenente il punto di inserimento) o, se è presente una selezione, il numero di riga della riga contenente l'inizio della selezione.</span><span class="sxs-lookup"><span data-stu-id="96d86-110">If this parameter is -1, **EM\_FILELINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="96d86-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96d86-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96d86-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="96d86-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d86-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96d86-113">Return value</span></span>

<span data-ttu-id="96d86-114">Il valore restituito è il numero di riga in base zero della riga che contiene l'indice dei caratteri specificato da *wParam*, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="96d86-114">The return value is the zero-based line number of the line containing the character index specified by *wParam*, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d86-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96d86-115">Requirements</span></span>



| <span data-ttu-id="96d86-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d86-116">Requirement</span></span> | <span data-ttu-id="96d86-117">Valore</span><span class="sxs-lookup"><span data-stu-id="96d86-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d86-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96d86-119">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="96d86-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="96d86-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96d86-121">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="96d86-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96d86-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96d86-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d86-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96d86-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96d86-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96d86-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="96d86-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="96d86-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96d86-126">**\_FILELINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="96d86-126">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





