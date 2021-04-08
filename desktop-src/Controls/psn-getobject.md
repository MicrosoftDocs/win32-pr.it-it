---
title: Codice di notifica PSN_GETOBJECT (Prsht. h)
description: Inviato da una finestra delle proprietà per richiedere un oggetto destinazione di rilascio quando il cursore passa su uno dei pulsanti del controllo struttura a schede. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- Controlli di Windows per il codice di notifica PSN_GETOBJECT
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048068"
---
# <a name="psn_getobject-notification-code"></a><span data-ttu-id="6d194-105">\_Codice di notifica GetObject PSN</span><span class="sxs-lookup"><span data-stu-id="6d194-105">PSN\_GETOBJECT notification code</span></span>

<span data-ttu-id="6d194-106">Inviato da una finestra delle proprietà per richiedere un oggetto destinazione di rilascio quando il cursore passa su uno dei pulsanti del controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="6d194-106">Sent by a property sheet to request a drop target object when the cursor passes over one of the tab control's buttons.</span></span> <span data-ttu-id="6d194-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6d194-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6d194-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d194-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d194-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d194-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d194-110">Puntatore a una struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) che, in ingresso, contiene informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="6d194-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that, on entry, contains information about the notification code.</span></span> <span data-ttu-id="6d194-111">Se il codice di notifica viene elaborato, è necessario inserire le informazioni sugli oggetti nella struttura.</span><span class="sxs-lookup"><span data-stu-id="6d194-111">If this notification code is processed, you must insert object information into this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d194-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d194-112">Return value</span></span>

<span data-ttu-id="6d194-113">L'elaborazione dell'applicazione del codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="6d194-113">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d194-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d194-114">Remarks</span></span>

<span data-ttu-id="6d194-115">Per fornire un oggetto, un'applicazione deve impostare i valori in alcuni membri della struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6d194-115">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="6d194-116">Il membro **pObject** deve essere impostato su un puntatore a un oggetto valido e il membro **HRESULT** deve essere impostato su un flag Success.</span><span class="sxs-lookup"><span data-stu-id="6d194-116">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="6d194-117">Per rispettare gli standard Component Object Model (COM), incrementare sempre il conteggio dei riferimenti dell'oggetto quando viene fornito un puntatore a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6d194-117">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="6d194-118">Se un'applicazione non fornisce un oggetto, deve impostare **pObject** su **null** e **HRESULT** su un flag di errore.</span><span class="sxs-lookup"><span data-stu-id="6d194-118">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

> [!Note]  
> <span data-ttu-id="6d194-119">Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="6d194-119">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d194-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d194-120">Requirements</span></span>



| <span data-ttu-id="6d194-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d194-121">Requirement</span></span> | <span data-ttu-id="6d194-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6d194-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d194-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d194-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d194-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d194-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d194-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d194-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d194-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d194-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d194-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d194-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d194-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d194-128"><dt>Prsht.h</dt></span></span> </dl> |



 

 





