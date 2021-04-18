---
title: Codice di notifica TCN_GETOBJECT (COMmctrl. h)
description: Inviato da un controllo struttura a schede quando dispone dello \_ \_ stile esteso TCS ex REGISTERDROP e un oggetto viene trascinato su un elemento di scheda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- Controlli di Windows per il codice di notifica TCN_GETOBJECT
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300963"
---
# <a name="tcn_getobject-notification-code"></a><span data-ttu-id="fd915-105">TCN \_ codice di notifica GETobject</span><span class="sxs-lookup"><span data-stu-id="fd915-105">TCN\_GETOBJECT notification code</span></span>

<span data-ttu-id="fd915-106">Inviato da un controllo struttura a schede quando dispone dello stile esteso [**TCS \_ ex \_ REGISTERDROP**](tab-control-extended-styles.md) e un oggetto viene trascinato su un elemento di scheda nel controllo.</span><span class="sxs-lookup"><span data-stu-id="fd915-106">Sent by a tab control when it has the [**TCS\_EX\_REGISTERDROP**](tab-control-extended-styles.md) extended style and an object is dragged over a tab item in the control.</span></span> <span data-ttu-id="fd915-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fd915-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fd915-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd915-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd915-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd915-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd915-110">Puntatore a una struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) che contiene informazioni sull'elemento di tabulazione su cui l'oggetto è stato trascinato e riceve i dati restituiti dall'applicazione in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="fd915-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the tab item the object is dragged over and receives data the application returns in response to this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd915-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd915-111">Return value</span></span>

<span data-ttu-id="fd915-112">L'elaborazione dell'applicazione del codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="fd915-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd915-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd915-113">Requirements</span></span>



| <span data-ttu-id="fd915-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd915-114">Requirement</span></span> | <span data-ttu-id="fd915-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fd915-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd915-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd915-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd915-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd915-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd915-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd915-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd915-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd915-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd915-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd915-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd915-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd915-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





