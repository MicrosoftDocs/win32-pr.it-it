---
description: Accetta una struttura STRRET restituita da IShellFolder::GetDisplayNameOf, la converte in una stringa e inserisce il risultato in un buffer.
title: Funzione StrRetToStrN
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
ms.openlocfilehash: 50295d712e539c94f10a708674cea595a47ae4e0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841032"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="9a2ad-103">Funzione StrRetToStrN</span><span class="sxs-lookup"><span data-stu-id="9a2ad-103">StrRetToStrN function</span></span>

<span data-ttu-id="9a2ad-104">Accetta una [**struttura STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) restituita da [**IShellFolder::GetDisplayNameOf,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)la converte in una stringa e inserisce il risultato in un buffer.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a2ad-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="9a2ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a2ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a2ad-107">*pszOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="9a2ad-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2ad-108">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="9a2ad-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="9a2ad-109">Buffer in cui contenere il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-109">Buffer to hold the display name.</span></span> <span data-ttu-id="9a2ad-110">Verrà restituito come stringa con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="9a2ad-111">Se *cchOut* è troppo piccolo, il nome verrà troncato per adattarsi.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="9a2ad-112">*cchOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9a2ad-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2ad-113">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="9a2ad-113">Type: **UINT**</span></span>

<span data-ttu-id="9a2ad-114">Dimensione di *pszOut,* in caratteri.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="9a2ad-115">Se *cchOut* è troppo piccolo, la stringa verrà troncata per adattarsi.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="9a2ad-116">*pStrRet* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9a2ad-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2ad-117">Tipo: **LPSTRRET**</span><span class="sxs-lookup"><span data-stu-id="9a2ad-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="9a2ad-118">Puntatore a una [**struttura STRRET.**](/windows/desktop/api/Shtypes/ns-shtypes-strret)</span><span class="sxs-lookup"><span data-stu-id="9a2ad-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="9a2ad-119">Quando la funzione viene restituita, questo puntatore non sarà più valido.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="9a2ad-120">*pidl* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9a2ad-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2ad-121">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="9a2ad-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="9a2ad-122">Puntatore alla struttura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a2ad-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a2ad-123">Return value</span></span>

<span data-ttu-id="9a2ad-124">Tipo: **BOOL**</span><span class="sxs-lookup"><span data-stu-id="9a2ad-124">Type: **BOOL**</span></span>

<span data-ttu-id="9a2ad-125">**TRUE per** l'esito positivo, **FALSE** per l'errore.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a2ad-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a2ad-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9a2ad-127">A Shell32.dll versione 5.0, chiamare questa funzione equivale a chiamare [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span><span class="sxs-lookup"><span data-stu-id="9a2ad-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="9a2ad-128">**StrRetToStrN** non viene esportato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="9a2ad-129">Per usarlo, è necessario usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 96 Shell32.dll per ottenere un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="9a2ad-130">Se il **membro uType** della struttura a cui punta *pStrRet* è impostato su **STRRET \_ WSTR,** il membro **pOleStr** di tale struttura verrà liberato in caso di restituzione.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="9a2ad-131">Si noti che questa funzione viene esportata da Shell32.dll anziché da Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="9a2ad-132">È incluso anche in Shlobj.h anziché in Shlwapi.h.</span><span class="sxs-lookup"><span data-stu-id="9a2ad-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a2ad-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a2ad-133">Requirements</span></span>



| <span data-ttu-id="9a2ad-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a2ad-134">Requirement</span></span> | <span data-ttu-id="9a2ad-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9a2ad-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2ad-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a2ad-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9a2ad-137">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9a2ad-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9a2ad-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a2ad-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9a2ad-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9a2ad-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9a2ad-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9a2ad-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a2ad-141"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="9a2ad-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a2ad-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a2ad-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a2ad-143">**StrRetToStr**</span><span class="sxs-lookup"><span data-stu-id="9a2ad-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="9a2ad-144">**StrRetToBuf**</span><span class="sxs-lookup"><span data-stu-id="9a2ad-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
