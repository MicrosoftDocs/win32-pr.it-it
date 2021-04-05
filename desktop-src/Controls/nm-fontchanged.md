---
title: Codice di notifica NM_FONTCHANGED (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando il controllo ha modificato un tipo di carattere. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- Controlli di Windows per il codice di notifica NM_FONTCHANGED
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75003021f83276c953b5aa2cf0b812d20d60857b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873306"
---
# <a name="nm_fontchanged-notification-code"></a><span data-ttu-id="94d7f-105">\_Codice di notifica FONTCHANGED Nm</span><span class="sxs-lookup"><span data-stu-id="94d7f-105">NM\_FONTCHANGED notification code</span></span>

<span data-ttu-id="94d7f-106">Inviato da un controllo di visualizzazione elenco quando il controllo ha modificato un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="94d7f-106">Sent by a list-view control when the control has changed a font.</span></span> <span data-ttu-id="94d7f-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="94d7f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="94d7f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="94d7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d7f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94d7f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94d7f-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="94d7f-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d7f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94d7f-111">Return value</span></span>

<span data-ttu-id="94d7f-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="94d7f-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d7f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94d7f-113">Requirements</span></span>



| <span data-ttu-id="94d7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d7f-114">Requirement</span></span> | <span data-ttu-id="94d7f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="94d7f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94d7f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d7f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="94d7f-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94d7f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94d7f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d7f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="94d7f-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94d7f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94d7f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94d7f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="94d7f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94d7f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





