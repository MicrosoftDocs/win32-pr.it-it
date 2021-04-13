---
title: Codice di notifica NM_CUSTOMTEXT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo informazioni sulle operazioni di testo personalizzate. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- Controlli di Windows per il codice di notifica NM_CUSTOMTEXT
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eebc4033a76d137e28a0c4170c5c613c7933562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400226"
---
# <a name="nm_customtext-notification-code"></a><span data-ttu-id="39bea-105">\_Codice di notifica CUSTOMTEXT Nm</span><span class="sxs-lookup"><span data-stu-id="39bea-105">NM\_CUSTOMTEXT notification code</span></span>

<span data-ttu-id="39bea-106">Notifica alla finestra padre di un controllo informazioni sulle operazioni di testo personalizzate.</span><span class="sxs-lookup"><span data-stu-id="39bea-106">Notifies a control's parent window about custom text operations.</span></span> <span data-ttu-id="39bea-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="39bea-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="39bea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="39bea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39bea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39bea-110">Puntatore a una struttura [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="39bea-110">A pointer to an [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39bea-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39bea-111">Return value</span></span>

<span data-ttu-id="39bea-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="39bea-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bea-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39bea-113">Requirements</span></span>



| <span data-ttu-id="39bea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39bea-114">Requirement</span></span> | <span data-ttu-id="39bea-115">Valore</span><span class="sxs-lookup"><span data-stu-id="39bea-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39bea-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39bea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39bea-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39bea-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39bea-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39bea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39bea-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39bea-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39bea-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39bea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39bea-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bea-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





