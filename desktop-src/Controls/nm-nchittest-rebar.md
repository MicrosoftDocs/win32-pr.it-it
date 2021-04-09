---
title: Codice di notifica di NM_NCHITTEST (Rebar) (COMmctrl. h)
description: Inviato da un controllo Rebar quando il controllo riceve un \_ messaggio WM NCHITTEST. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST (Rebar) il codice di notifica controlli Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120715"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="7df88-105">\_Codice di notifica NCHITTEST (Rebar) Nm</span><span class="sxs-lookup"><span data-stu-id="7df88-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="7df88-106">Inviato da un controllo Rebar quando il controllo riceve un messaggio [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="7df88-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="7df88-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7df88-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7df88-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7df88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df88-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7df88-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7df88-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="7df88-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="7df88-111">Il membro **dwItemSpec** contiene l'indice della banda su cui si è verificato il messaggio di hit test e il membro **PT** contiene le coordinate del mouse del messaggio di hit test.</span><span class="sxs-lookup"><span data-stu-id="7df88-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df88-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7df88-112">Return value</span></span>

<span data-ttu-id="7df88-113">Restituisce zero per consentire al rebar di eseguire l'elaborazione predefinita del messaggio di hit test oppure restituire uno dei valori HT \* documentati in [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) per eseguire l'override dell'elaborazione dell'hit test predefinita.</span><span class="sxs-lookup"><span data-stu-id="7df88-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df88-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7df88-114">Requirements</span></span>



| <span data-ttu-id="7df88-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df88-115">Requirement</span></span> | <span data-ttu-id="7df88-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7df88-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7df88-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7df88-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7df88-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7df88-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7df88-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7df88-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7df88-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7df88-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7df88-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7df88-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7df88-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7df88-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

