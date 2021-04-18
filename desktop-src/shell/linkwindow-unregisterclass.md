---
description: Annulla la registrazione di una classe di finestra registrata da LinkWindow \_ registerClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: Funzione LinkWindow_UnregisterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980018"
---
# <a name="linkwindow_unregisterclass-function"></a><span data-ttu-id="e05cb-103">LinkWindow \_ UnregisterClass-funzione</span><span class="sxs-lookup"><span data-stu-id="e05cb-103">LinkWindow\_UnregisterClass function</span></span>

<span data-ttu-id="e05cb-104">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e05cb-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="e05cb-105">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e05cb-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e05cb-106">Annulla la registrazione di una classe di finestra registrata da [**LinkWindow \_ registerClass**](linkwindow-registerclass.md).</span><span class="sxs-lookup"><span data-stu-id="e05cb-106">Unregisters a window class registered by [**LinkWindow\_RegisterClass**](linkwindow-registerclass.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e05cb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e05cb-107">Syntax</span></span>


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="e05cb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e05cb-108">Parameters</span></span>

<span data-ttu-id="e05cb-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="e05cb-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e05cb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e05cb-110">Return value</span></span>

<span data-ttu-id="e05cb-111">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="e05cb-111">Type: **BOOL**</span></span>

<span data-ttu-id="e05cb-112">Restituisce **true** se l'operazione è stata eseguita correttamente. In caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="e05cb-112">Returns **TRUE** if the operation was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e05cb-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e05cb-113">Remarks</span></span>

<span data-ttu-id="e05cb-114">Questa funzione non dispone di un file di intestazione o di libreria associato, quindi deve essere chiamata in base al valore ordinale.</span><span class="sxs-lookup"><span data-stu-id="e05cb-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="e05cb-115">Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della dll Shell32.dll per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="e05cb-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="e05cb-116">Chiamare quindi [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle di modulo e il numero ordinale 259 per usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="e05cb-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 259 to use this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e05cb-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e05cb-117">Requirements</span></span>



| <span data-ttu-id="e05cb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e05cb-118">Requirement</span></span> | <span data-ttu-id="e05cb-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e05cb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e05cb-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e05cb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e05cb-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e05cb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e05cb-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e05cb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e05cb-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e05cb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e05cb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e05cb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e05cb-125"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e05cb-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e05cb-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e05cb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e05cb-127">Panoramica dei controlli SysLink</span><span class="sxs-lookup"><span data-stu-id="e05cb-127">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
