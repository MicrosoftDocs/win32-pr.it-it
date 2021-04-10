---
description: Un'applicazione invia il \_ messaggio WM WININICHANGE a tutte le finestre di primo livello dopo avere apportato una modifica al file di WIN.INI. La funzione SystemParametersInfo Invia questo messaggio dopo che un'applicazione usa la funzione per modificare un'impostazione in WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Messaggio WM_WININICHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966645"
---
# <a name="wm_wininichange-message"></a><span data-ttu-id="33526-104">\_Messaggio WININICHANGE WM</span><span class="sxs-lookup"><span data-stu-id="33526-104">WM\_WININICHANGE message</span></span>

<span data-ttu-id="33526-105">Un'applicazione invia il messaggio **WM \_ WININICHANGE** a tutte le finestre di primo livello dopo avere apportato una modifica al file di WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="33526-105">An application sends the **WM\_WININICHANGE** message to all top-level windows after making a change to the WIN.INI file.</span></span> <span data-ttu-id="33526-106">La funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) Invia questo messaggio dopo che un'applicazione usa la funzione per modificare un'impostazione in WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="33526-106">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function sends this message after an application uses the function to change a setting in WIN.INI.</span></span>

> [!Note]  
> <span data-ttu-id="33526-107">Il messaggio **WM \_ WININICHANGE** viene fornito solo per la compatibilità con le versioni precedenti del sistema.</span><span class="sxs-lookup"><span data-stu-id="33526-107">The **WM\_WININICHANGE** message is provided only for compatibility with earlier versions of the system.</span></span> <span data-ttu-id="33526-108">Le applicazioni devono usare il messaggio [**WM \_ SETTINGCHANGE**](wm-settingchange.md) .</span><span class="sxs-lookup"><span data-stu-id="33526-108">Applications should use the [**WM\_SETTINGCHANGE**](wm-settingchange.md) message.</span></span>

 

<span data-ttu-id="33526-109">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="33526-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a><span data-ttu-id="33526-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="33526-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33526-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33526-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33526-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="33526-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="33526-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33526-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33526-114">Puntatore a una stringa contenente il nome del parametro di sistema che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="33526-114">A pointer to a string containing the name of the system parameter that was changed.</span></span> <span data-ttu-id="33526-115">Questa stringa, ad esempio, può essere il nome di una chiave del registro di sistema o il nome di una sezione nel file di Win.ini.</span><span class="sxs-lookup"><span data-stu-id="33526-115">For example, this string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="33526-116">Questo parametro non è particolarmente utile per determinare quale parametro di sistema è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="33526-116">This parameter is not particularly useful in determining which system parameter changed.</span></span> <span data-ttu-id="33526-117">Ad esempio, quando la stringa è un nome del registro di sistema, in genere indica solo il nodo foglia nel registro di sistema, non l'intero percorso.</span><span class="sxs-lookup"><span data-stu-id="33526-117">For example, when the string is a registry name, it typically indicates only the leaf node in the registry, not the whole path.</span></span> <span data-ttu-id="33526-118">Inoltre, alcune applicazioni inviano questo messaggio con *lParam* impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="33526-118">In addition, some applications send this message with *lParam* set to **NULL**.</span></span> <span data-ttu-id="33526-119">In generale, quando si riceve questo messaggio, è necessario controllare e ricaricare le impostazioni dei parametri di sistema utilizzate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="33526-119">In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33526-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33526-120">Return value</span></span>

<span data-ttu-id="33526-121">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="33526-121">Type: **LRESULT**</span></span>

<span data-ttu-id="33526-122">Se si elabora questo messaggio, restituire zero.</span><span class="sxs-lookup"><span data-stu-id="33526-122">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="33526-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="33526-123">Remarks</span></span>

<span data-ttu-id="33526-124">Per inviare il **messaggio \_ WM WININICHANGE** a tutte le finestre di primo livello, utilizzare la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con il parametro *HWND* impostato su **HWND \_ broadcast**.</span><span class="sxs-lookup"><span data-stu-id="33526-124">To send the **WM\_WININICHANGE** message to all top-level windows, use the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the *hWnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="33526-125">In alternativa, è possibile eseguire il mapping delle chiamate a funzioni che cambiano WIN.INI al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="33526-125">Calls to functions that change WIN.INI may be mapped to the registry instead.</span></span> <span data-ttu-id="33526-126">Questo mapping si verifica quando WIN.INI e la sezione da modificare vengono specificati nel registro di sistema con la seguente chiave:</span><span class="sxs-lookup"><span data-stu-id="33526-126">This mapping occurs when WIN.INI and the section being changed are specified in the registry under the following key:</span></span>

<span data-ttu-id="33526-127">**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**</span><span class="sxs-lookup"><span data-stu-id="33526-127">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\IniFileMapping**</span></span>

<span data-ttu-id="33526-128">La modifica nel percorso di archiviazione non ha alcun effetto sul comportamento di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="33526-128">The change in the storage location has no effect on the behavior of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="33526-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33526-129">Requirements</span></span>



| <span data-ttu-id="33526-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="33526-130">Requirement</span></span> | <span data-ttu-id="33526-131">Valore</span><span class="sxs-lookup"><span data-stu-id="33526-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33526-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33526-132">Minimum supported client</span></span><br/> | <span data-ttu-id="33526-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33526-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="33526-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33526-134">Minimum supported server</span></span><br/> | <span data-ttu-id="33526-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33526-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33526-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33526-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="33526-137"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33526-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33526-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33526-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33526-139">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="33526-139">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
