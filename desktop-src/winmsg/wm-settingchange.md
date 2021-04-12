---
description: Messaggio inviato a tutte le finestre di primo livello quando la funzione SystemParametersInfo modifica un'impostazione a livello di sistema o quando sono state modificate le impostazioni dei criteri.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Messaggio WM_SETTINGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233715"
---
# <a name="wm_settingchange-message"></a><span data-ttu-id="5e0b7-103">\_Messaggio SETTINGCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="5e0b7-103">WM\_SETTINGCHANGE message</span></span>

<span data-ttu-id="5e0b7-104">Messaggio inviato a tutte le finestre di primo livello quando la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) modifica un'impostazione a livello di sistema o quando sono state modificate le impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-104">A message that is sent to all top-level windows when the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function changes a system-wide setting or when policy settings have changed.</span></span>

<span data-ttu-id="5e0b7-105">Le applicazioni devono inviare **WM \_ SETTINGCHANGE** a tutte le finestre di primo livello quando apportano modifiche ai parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-105">Applications should send **WM\_SETTINGCHANGE** to all top-level windows when they make changes to system parameters.</span></span> <span data-ttu-id="5e0b7-106">(Questo messaggio non può essere inviato direttamente a una finestra). Per inviare il **messaggio \_ WM SETTINGCHANGE** a tutte le finestre di primo livello, utilizzare la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con il parametro *HWND* impostato su **HWND \_ broadcast**.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-106">(This message cannot be sent directly to a window.) To send the **WM\_SETTINGCHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hwnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="5e0b7-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5e0b7-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a><span data-ttu-id="5e0b7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e0b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e0b7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e0b7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e0b7-110">Quando il sistema invia questo messaggio in seguito a una chiamata [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , il parametro *wParam* corrisponde al valore del parametro *uiAction* passato alla funzione **SystemParametersInfo** .</span><span class="sxs-lookup"><span data-stu-id="5e0b7-110">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, the *wParam* parameter is the value of the *uiAction* parameter passed to the **SystemParametersInfo** function.</span></span> <span data-ttu-id="5e0b7-111">Per un elenco di valori, vedere **SystemParametersInfo**.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-111">For a list of values, see **SystemParametersInfo**.</span></span>

<span data-ttu-id="5e0b7-112">Quando il sistema invia questo messaggio a seguito di una modifica nelle impostazioni dei criteri, questo parametro indica il tipo di criteri applicato.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-112">When the system sends this message as a result of a change in policy settings, this parameter indicates the type of policy that was applied.</span></span> <span data-ttu-id="5e0b7-113">Questo valore è 1 se è stato applicato un criterio computer o zero se è stato applicato un criterio utente.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-113">This value is 1 if computer policy was applied or zero if user policy was applied.</span></span>

<span data-ttu-id="5e0b7-114">Quando il sistema invia questo messaggio a seguito di una modifica nelle impostazioni locali, questo parametro è zero.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-114">When the system sends this message as a result of a change in locale settings, this parameter is zero.</span></span>

<span data-ttu-id="5e0b7-115">Quando un'applicazione invia questo messaggio, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-115">When an application sends this message, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5e0b7-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e0b7-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e0b7-117">Quando il sistema invia questo messaggio in seguito a una chiamata [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* è un puntatore a una stringa che indica l'area contenente il parametro di sistema che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-117">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, *lParam* is a pointer to a string that indicates the area containing the system parameter that was changed.</span></span> <span data-ttu-id="5e0b7-118">Questo parametro non indica in genere quale parametro di sistema specifico è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-118">This parameter does not usually indicate which specific system parameter changed.</span></span> <span data-ttu-id="5e0b7-119">Si noti che alcune applicazioni inviano questo messaggio con *lParam* impostato su **null**. In generale, quando si riceve questo messaggio, è necessario controllare e ricaricare le impostazioni dei parametri di sistema utilizzate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-119">(Note that some applications send this message with *lParam* set to **NULL**.) In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

<span data-ttu-id="5e0b7-120">Questa stringa può essere il nome di una chiave del registro di sistema o il nome di una sezione nel file di Win.ini.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-120">This string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="5e0b7-121">Quando la stringa è un nome del registro di sistema, in genere indica solo il nodo foglia nel registro di sistema, non il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-121">When the string is a registry name, it typically indicates only the leaf node in the registry, not the full path.</span></span>

<span data-ttu-id="5e0b7-122">Quando il sistema invia questo messaggio a seguito di una modifica nelle impostazioni dei criteri, questo parametro punta alla stringa "Policy".</span><span class="sxs-lookup"><span data-stu-id="5e0b7-122">When the system sends this message as a result of a change in policy settings, this parameter points to the string "Policy".</span></span>

<span data-ttu-id="5e0b7-123">Quando il sistema invia questo messaggio a seguito di una modifica nelle impostazioni locali, questo parametro punta alla stringa "Intl".</span><span class="sxs-lookup"><span data-stu-id="5e0b7-123">When the system sends this message as a result of a change in locale settings, this parameter points to the string "intl".</span></span>

<span data-ttu-id="5e0b7-124">Per applicare una modifica nelle variabili di ambiente per il sistema o l'utente, trasmettere questo messaggio con *lParam* impostato sulla stringa "Environment".</span><span class="sxs-lookup"><span data-stu-id="5e0b7-124">To effect a change in the environment variables for the system or the user, broadcast this message with *lParam* set to the string "Environment".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e0b7-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e0b7-125">Return value</span></span>

<span data-ttu-id="5e0b7-126">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e0b7-126">Type: **LRESULT**</span></span>

<span data-ttu-id="5e0b7-127">Se si elabora questo messaggio, restituire zero.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-127">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e0b7-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e0b7-128">Remarks</span></span>

<span data-ttu-id="5e0b7-129">Il parametro *lParam* indica quale metrica di sistema è stata modificata, ad esempio, "ConvertibleSlateMode" se l'indicatore ConvertibleSlateMode è stato attivato o "SystemDockMode" se l'indicatore ancorato è stato attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="5e0b7-129">The *lParam* parameter indicates which system metric has changed, for example, "ConvertibleSlateMode" if the CONVERTIBLESLATEMODE indicator was toggled or "SystemDockMode" if the DOCKED indicator was toggled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e0b7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e0b7-130">Requirements</span></span>



| <span data-ttu-id="5e0b7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e0b7-131">Requirement</span></span> | <span data-ttu-id="5e0b7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5e0b7-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e0b7-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e0b7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5e0b7-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e0b7-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5e0b7-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e0b7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5e0b7-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e0b7-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e0b7-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e0b7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e0b7-138"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e0b7-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e0b7-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e0b7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e0b7-140">Eventi dei criteri</span><span class="sxs-lookup"><span data-stu-id="5e0b7-140">Policy Events</span></span>](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[<span data-ttu-id="5e0b7-141">**SendMessageTimeout**</span><span class="sxs-lookup"><span data-stu-id="5e0b7-141">**SendMessageTimeout**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[<span data-ttu-id="5e0b7-142">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="5e0b7-142">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
