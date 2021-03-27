---
description: 'Accetta una struttura STRRET restituita da IShellFolder:: GetDisplayNameOf, la converte in una stringa e inserisce il risultato in un buffer.'
title: StrRetToStrN (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995173"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="c7871-103">StrRetToStrN (funzione)</span><span class="sxs-lookup"><span data-stu-id="c7871-103">StrRetToStrN function</span></span>

<span data-ttu-id="c7871-104">Accetta una struttura [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) restituita da [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), la converte in una stringa e inserisce il risultato in un buffer.</span><span class="sxs-lookup"><span data-stu-id="c7871-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7871-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7871-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="c7871-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7871-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7871-107">*pszOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c7871-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7871-108">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="c7871-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="c7871-109">Buffer in cui memorizzare il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c7871-109">Buffer to hold the display name.</span></span> <span data-ttu-id="c7871-110">Verrà restituito come stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="c7871-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="c7871-111">Se *cchOut* è troppo piccolo, il nome verrà troncato per adattarlo.</span><span class="sxs-lookup"><span data-stu-id="c7871-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="c7871-112">*cchOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7871-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7871-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c7871-113">Type: **UINT**</span></span>

<span data-ttu-id="c7871-114">Dimensioni di *pszOut*, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="c7871-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="c7871-115">Se *cchOut* è troppo piccolo, la stringa verrà troncata per essere adattata.</span><span class="sxs-lookup"><span data-stu-id="c7871-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="c7871-116">*pStrRet* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="c7871-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7871-117">Tipo: **LPSTRRET**</span><span class="sxs-lookup"><span data-stu-id="c7871-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="c7871-118">Puntatore a una struttura [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) .</span><span class="sxs-lookup"><span data-stu-id="c7871-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="c7871-119">Quando la funzione restituisce, il puntatore non sarà più valido.</span><span class="sxs-lookup"><span data-stu-id="c7871-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="c7871-120">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7871-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7871-121">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="c7871-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="c7871-122">Puntatore alla struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c7871-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7871-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7871-123">Return value</span></span>

<span data-ttu-id="c7871-124">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="c7871-124">Type: **BOOL**</span></span>

<span data-ttu-id="c7871-125">**True** per l'esito positivo, **false** per l'errore.</span><span class="sxs-lookup"><span data-stu-id="c7871-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7871-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7871-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c7871-127">A partire da Shell32.dll versione 5,0, la chiamata a questa funzione equivale alla chiamata a [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span><span class="sxs-lookup"><span data-stu-id="c7871-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="c7871-128">**StrRetToStrN** non viene esportato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c7871-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="c7871-129">Per usarlo, è necessario usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 96 da Shell32.dll per ottenere un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="c7871-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="c7871-130">Se il membro **uType** della struttura a cui punta *pStrRet* è impostato su **STRRET \_ WSTR**, il membro **pOleStr** di tale struttura verrà liberato al ritorno.</span><span class="sxs-lookup"><span data-stu-id="c7871-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="c7871-131">Si noti che questa funzione viene esportata da Shell32.dll anziché da Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="c7871-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="c7871-132">È incluso anche in Shlobj. h anziché in Shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="c7871-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7871-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7871-133">Requirements</span></span>



| <span data-ttu-id="c7871-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7871-134">Requirement</span></span> | <span data-ttu-id="c7871-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c7871-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7871-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7871-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c7871-137">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c7871-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c7871-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7871-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c7871-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c7871-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c7871-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c7871-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7871-141"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="c7871-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7871-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7871-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7871-143">**StrRetToStr**</span><span class="sxs-lookup"><span data-stu-id="c7871-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="c7871-144">**StrRetToBuf**</span><span class="sxs-lookup"><span data-stu-id="c7871-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
