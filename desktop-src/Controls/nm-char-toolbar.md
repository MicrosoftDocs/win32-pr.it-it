---
title: Codice di notifica NM_CHAR (barra degli strumenti) (COMmctrl. h)
description: Inviato da una barra degli strumenti quando riceve un \_ messaggio WM Char. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- Codice di notifica di NM_CHAR (barra degli strumenti) controlli Windows
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874697"
---
# <a name="nm_char-toolbar-notification-code"></a><span data-ttu-id="1f1d9-105">Codice di notifica di NM \_ char (barra degli strumenti)</span><span class="sxs-lookup"><span data-stu-id="1f1d9-105">NM\_CHAR (toolbar) notification code</span></span>

<span data-ttu-id="1f1d9-106">Inviato da una barra degli strumenti quando riceve un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="1f1d9-106">Sent by a toolbar when it receives a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span> <span data-ttu-id="1f1d9-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1f1d9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1f1d9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f1d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f1d9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f1d9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f1d9-110">Puntatore a una struttura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) contenente informazioni aggiuntive sul carattere che ha causato il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-110">Pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span> <span data-ttu-id="1f1d9-111">Il membro **dwItemPrev** della struttura contiene l'identificatore di comando dell'elemento attualmente attivo o-1 se nessun elemento è attualmente attivo.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-111">The **dwItemPrev** member of this structure contains the command identifier of the item that is currently hot or -1 if no item is currently hot.</span></span> <span data-ttu-id="1f1d9-112">Il membro **dwItemNext** di questa struttura contiene l'identificatore di comando dell'elemento che diventerà attivo o-1 se la chiave non corrisponde al tasto di scelta rapida di un elemento.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-112">The **dwItemNext** member of this structure contains the command identifier of the item that will become hot or -1 if the key does not match any item's accelerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f1d9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f1d9-113">Return value</span></span>

<span data-ttu-id="1f1d9-114">Restituisce **true** per indicare che la barra degli strumenti non deve elaborare il carattere e **false** per fare in modo che la barra degli strumenti elabori il carattere.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-114">Returns **TRUE** to indicate that the toolbar should not process the character and **FALSE** to have the toolbar process the character.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f1d9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f1d9-115">Requirements</span></span>



| <span data-ttu-id="1f1d9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f1d9-116">Requirement</span></span> | <span data-ttu-id="1f1d9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1f1d9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1d9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f1d9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f1d9-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f1d9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f1d9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f1d9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f1d9-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f1d9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f1d9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f1d9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f1d9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f1d9-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

