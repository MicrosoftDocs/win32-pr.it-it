---
description: Un'applicazione invia il \_ messaggio WM FONTCHANGE a tutte le finestre di primo livello nel sistema dopo aver modificato il pool di risorse del tipo di carattere.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Messaggio WM_FONTCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980287"
---
# <a name="wm_fontchange-message"></a><span data-ttu-id="74cd9-103">\_Messaggio FONTCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="74cd9-103">WM\_FONTCHANGE message</span></span>

<span data-ttu-id="74cd9-104">Un'applicazione invia il messaggio **WM \_ FONTCHANGE** a tutte le finestre di primo livello nel sistema dopo aver modificato il pool di risorse del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="74cd9-104">An application sends the **WM\_FONTCHANGE** message to all top-level windows in the system after changing the pool of font resources.</span></span>

<span data-ttu-id="74cd9-105">Per inviare questo messaggio, chiamare la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="74cd9-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="74cd9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74cd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74cd9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74cd9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74cd9-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="74cd9-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74cd9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74cd9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74cd9-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="74cd9-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74cd9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="74cd9-111">Remarks</span></span>

<span data-ttu-id="74cd9-112">Un'applicazione che aggiunge o rimuove i tipi di carattere dal sistema, ad esempio tramite la funzione [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) , deve inviare questo messaggio a tutte le finestre di primo livello.</span><span class="sxs-lookup"><span data-stu-id="74cd9-112">An application that adds or removes fonts from the system (for example, by using the [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) or [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) function) should send this message to all top-level windows.</span></span>

<span data-ttu-id="74cd9-113">Per inviare il messaggio **WM \_ FONTCHANGE** a tutte le finestre di primo livello, un'applicazione può chiamare la funzione **SendMessage** con il parametro *HWND* impostato su HWND \_ broadcast.</span><span class="sxs-lookup"><span data-stu-id="74cd9-113">To send the **WM\_FONTCHANGE** message to all top-level windows, an application can call the **SendMessage** function with the *hwnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="74cd9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74cd9-114">Requirements</span></span>



| <span data-ttu-id="74cd9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="74cd9-115">Requirement</span></span> | <span data-ttu-id="74cd9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="74cd9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74cd9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74cd9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="74cd9-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74cd9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="74cd9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74cd9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="74cd9-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74cd9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74cd9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74cd9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="74cd9-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74cd9-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74cd9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74cd9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74cd9-124">Cenni preliminari su tipi di carattere e testo</span><span class="sxs-lookup"><span data-stu-id="74cd9-124">Fonts and Text Overview</span></span>](fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="74cd9-125">Tipi di carattere e messaggi di testo</span><span class="sxs-lookup"><span data-stu-id="74cd9-125">Font and Text Messages</span></span>](font-and-text-messages.md)
</dt> <dt>

[<span data-ttu-id="74cd9-126">**AddFontResource**</span><span class="sxs-lookup"><span data-stu-id="74cd9-126">**AddFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[<span data-ttu-id="74cd9-127">**RemoveFontResource**</span><span class="sxs-lookup"><span data-stu-id="74cd9-127">**RemoveFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
