---
title: Codice di notifica TBN_GETOBJECT (COMmctrl. h)
description: Inviato da un controllo Toolbar che usa lo \_ stile REGISTERDROP TBSTYLE per richiedere un oggetto destinazione di rilascio quando il puntatore passa su uno dei pulsanti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- Controlli di Windows per il codice di notifica TBN_GETOBJECT
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118966"
---
# <a name="tbn_getobject-notification-code"></a><span data-ttu-id="b13ec-105">TBN \_ codice di notifica GETobject</span><span class="sxs-lookup"><span data-stu-id="b13ec-105">TBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="b13ec-106">Inviato da un controllo Toolbar che usa lo [**stile \_ REGISTERDROP TBSTYLE**](toolbar-control-and-button-styles.md) per richiedere un oggetto destinazione di rilascio quando il puntatore passa su uno dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="b13ec-106">Sent by a toolbar control that uses the [**TBSTYLE\_REGISTERDROP**](toolbar-control-and-button-styles.md) style to request a drop target object when the pointer passes over one of its buttons.</span></span> <span data-ttu-id="b13ec-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b13ec-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b13ec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b13ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b13ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b13ec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b13ec-110">Puntatore a una struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) contenente informazioni sul pulsante passato dal puntatore e che riceve i dati forniti dall'applicazione in risposta a questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="b13ec-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the button that the pointer passed over and receives data the application provides in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b13ec-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b13ec-111">Return value</span></span>

<span data-ttu-id="b13ec-112">L'elaborazione dell'applicazione del codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="b13ec-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b13ec-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b13ec-113">Remarks</span></span>

<span data-ttu-id="b13ec-114">Per fornire un oggetto, un'applicazione deve impostare i valori in alcuni membri della struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="b13ec-114">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="b13ec-115">Il membro **pObject** deve essere impostato su un puntatore a un oggetto valido e il membro **HRESULT** deve essere impostato su un flag Success.</span><span class="sxs-lookup"><span data-stu-id="b13ec-115">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="b13ec-116">Per rispettare gli standard Component Object Model (COM), incrementare sempre il conteggio dei riferimenti dell'oggetto quando viene fornito un puntatore a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b13ec-116">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="b13ec-117">Se un'applicazione non fornisce un oggetto, deve impostare **pObject** su **null** e **HRESULT** su un flag di errore.</span><span class="sxs-lookup"><span data-stu-id="b13ec-117">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="b13ec-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b13ec-118">Requirements</span></span>



| <span data-ttu-id="b13ec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b13ec-119">Requirement</span></span> | <span data-ttu-id="b13ec-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b13ec-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b13ec-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b13ec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b13ec-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b13ec-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b13ec-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b13ec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b13ec-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b13ec-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b13ec-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b13ec-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b13ec-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b13ec-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





