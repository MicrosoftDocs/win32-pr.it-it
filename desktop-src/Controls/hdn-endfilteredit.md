---
title: Codice di notifica HDN_ENDFILTEREDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che è terminata la modifica di un filtro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d3832875-4cde-4d8a-b3a4-a8dae0742c56
keywords:
- Controlli di Windows per il codice di notifica HDN_ENDFILTEREDIT
topic_type:
- apiref
api_name:
- HDN_ENDFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a557278598600f1bd11ebfbe791691de954a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744010"
---
# <a name="hdn_endfilteredit-notification-code"></a><span data-ttu-id="4a542-105">\_Codice di notifica ENDFILTEREDIT di HDN</span><span class="sxs-lookup"><span data-stu-id="4a542-105">HDN\_ENDFILTEREDIT notification code</span></span>

<span data-ttu-id="4a542-106">Notifica alla finestra padre di un controllo di intestazione che è terminata la modifica di un filtro.</span><span class="sxs-lookup"><span data-stu-id="4a542-106">Notifies a header control's parent window that a filter edit has ended.</span></span> <span data-ttu-id="4a542-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4a542-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4a542-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a542-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a542-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a542-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a542-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni aggiuntive sul filtro in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="4a542-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a542-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a542-111">Return value</span></span>

<span data-ttu-id="4a542-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="4a542-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a542-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a542-113">Requirements</span></span>



| <span data-ttu-id="4a542-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a542-114">Requirement</span></span> | <span data-ttu-id="4a542-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4a542-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a542-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a542-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a542-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a542-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a542-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a542-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a542-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a542-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a542-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a542-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a542-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a542-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





