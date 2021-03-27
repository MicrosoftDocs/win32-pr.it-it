---
description: Registra una classe della finestra che consente l'uso del controllo comune SysLink in una finestra.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: Funzione LinkWindow_RegisterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980023"
---
# <a name="linkwindow_registerclass-function"></a><span data-ttu-id="70547-103">\_Funzione LinkWindow registerClass</span><span class="sxs-lookup"><span data-stu-id="70547-103">LinkWindow\_RegisterClass function</span></span>

<span data-ttu-id="70547-104">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70547-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="70547-105">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="70547-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="70547-106">In alternativa, usare [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) .\]</span><span class="sxs-lookup"><span data-stu-id="70547-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) instead.\]</span></span>

<span data-ttu-id="70547-107">Registra una classe della finestra che consente l'uso del controllo comune [Syslink](../controls/syslink-overview.md) in una finestra.</span><span class="sxs-lookup"><span data-stu-id="70547-107">Registers a window class that allows for the [SysLink](../controls/syslink-overview.md) common control to be used in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="70547-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70547-108">Syntax</span></span>


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="70547-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="70547-109">Parameters</span></span>

<span data-ttu-id="70547-110">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="70547-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70547-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70547-111">Return value</span></span>

<span data-ttu-id="70547-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="70547-112">Type: **BOOL**</span></span>

<span data-ttu-id="70547-113">Restituisce **true** se la registrazione è stata eseguita correttamente. In caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="70547-113">Returns **TRUE** if registration was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="70547-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="70547-114">Remarks</span></span>

<span data-ttu-id="70547-115">Questa funzione non dispone di un file di intestazione o di libreria associato, quindi deve essere chiamata in base al valore ordinale.</span><span class="sxs-lookup"><span data-stu-id="70547-115">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="70547-116">Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della dll Shell32.dll per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="70547-116">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="70547-117">Chiamare quindi [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle di modulo e il numero ordinale 258 per usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="70547-117">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 258 to use this function.</span></span>

<span data-ttu-id="70547-118">Utilizzare [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) per annullare la registrazione della classe dopo l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="70547-118">Use [**LinkWindow\_UnregisterClass**](linkwindow-unregisterclass.md) to unregister the class after use.</span></span>

## <a name="requirements"></a><span data-ttu-id="70547-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70547-119">Requirements</span></span>



| <span data-ttu-id="70547-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="70547-120">Requirement</span></span> | <span data-ttu-id="70547-121">Valore</span><span class="sxs-lookup"><span data-stu-id="70547-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70547-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70547-122">Minimum supported client</span></span><br/> | <span data-ttu-id="70547-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70547-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70547-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70547-124">Minimum supported server</span></span><br/> | <span data-ttu-id="70547-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70547-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="70547-126">DLL</span><span class="sxs-lookup"><span data-stu-id="70547-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70547-127"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="70547-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70547-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70547-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70547-129">Panoramica dei controlli SysLink</span><span class="sxs-lookup"><span data-stu-id="70547-129">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
