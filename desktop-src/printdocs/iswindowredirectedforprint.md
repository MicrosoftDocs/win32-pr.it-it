---
description: La funzione IsWindowRedirectedForPrint determina se la finestra specificata è attualmente reindirizzata per la stampa.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: IsWindowRedirectedForPrint (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318371"
---
# <a name="iswindowredirectedforprint-function"></a><span data-ttu-id="cb000-103">IsWindowRedirectedForPrint (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb000-103">IsWindowRedirectedForPrint function</span></span>

<span data-ttu-id="cb000-104">La funzione **IsWindowRedirectedForPrint** determina se la finestra specificata è attualmente reindirizzata per la stampa.</span><span class="sxs-lookup"><span data-stu-id="cb000-104">The **IsWindowRedirectedForPrint** function determines whether the specified window is currently redirected for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb000-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb000-105">Syntax</span></span>


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="cb000-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb000-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb000-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb000-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb000-108">Handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="cb000-108">The handle of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb000-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb000-109">Return value</span></span>

<span data-ttu-id="cb000-110">Se la finestra è attualmente reindirizzata per la stampa, la funzione restituisce un valore diverso da zero. in caso contrario, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="cb000-110">If the window is currently redirected for printing, the function returns a nonzero value; otherwise, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb000-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb000-111">Remarks</span></span>

<span data-ttu-id="cb000-112">Una finestra viene reindirizzata per la stampa quando elabora una chiamata a [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span><span class="sxs-lookup"><span data-stu-id="cb000-112">A window is redirected for printing when it processes a call to [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span></span> <span data-ttu-id="cb000-113">In una chiamata a **PrintWindow**, una finestra esegue il rendering del contenuto in un contesto di dispositivo fuori schermo.</span><span class="sxs-lookup"><span data-stu-id="cb000-113">In a call to **PrintWindow**, a window renders its content to an off-screen device context.</span></span>

<span data-ttu-id="cb000-114">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="cb000-114">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb000-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb000-115">Requirements</span></span>



| <span data-ttu-id="cb000-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb000-116">Requirement</span></span> | <span data-ttu-id="cb000-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cb000-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb000-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb000-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb000-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb000-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb000-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb000-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb000-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb000-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb000-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cb000-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb000-123"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb000-123"><dt>User32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb000-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb000-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb000-125">**PrintWindow**</span><span class="sxs-lookup"><span data-stu-id="cb000-125">**PrintWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[<span data-ttu-id="cb000-126">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="cb000-126">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="cb000-127">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="cb000-127">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="cb000-128">**\_stampa WM**</span><span class="sxs-lookup"><span data-stu-id="cb000-128">**WM\_PRINT**</span></span>](/windows/desktop/gdi/wm-print)
</dt> <dt>

[<span data-ttu-id="cb000-129">**\_PRINTCLIENT WM**</span><span class="sxs-lookup"><span data-stu-id="cb000-129">**WM\_PRINTCLIENT**</span></span>](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

