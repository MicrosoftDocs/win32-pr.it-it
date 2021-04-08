---
title: Funzione Str_GetPtr
description: Copia una stringa da un buffer a un altro.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Controlli di Windows per la funzione Str_GetPtr
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740511"
---
# <a name="str_getptr-function"></a><span data-ttu-id="995ba-104">Str \_ Getptr (funzione)</span><span class="sxs-lookup"><span data-stu-id="995ba-104">Str\_GetPtr function</span></span>

<span data-ttu-id="995ba-105">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="995ba-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="995ba-106">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="995ba-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="995ba-107">Copia una stringa da un buffer a un altro.</span><span class="sxs-lookup"><span data-stu-id="995ba-107">Copies a string from one buffer to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="995ba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="995ba-108">Syntax</span></span>


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a><span data-ttu-id="995ba-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="995ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="995ba-110">*pszSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="995ba-110">*pszSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="995ba-111">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="995ba-111">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="995ba-112">Puntatore a una stringa di origine.</span><span class="sxs-lookup"><span data-stu-id="995ba-112">A pointer to a source string.</span></span>

</dd> <dt>

<span data-ttu-id="995ba-113">*pszDest* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="995ba-113">*pszDest* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="995ba-114">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="995ba-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="995ba-115">Puntatore al buffer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="995ba-115">A pointer to the destination buffer.</span></span> <span data-ttu-id="995ba-116">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="995ba-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="995ba-117">*cchDest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="995ba-117">*cchDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="995ba-118">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="995ba-118">Type: **int**</span></span>

<span data-ttu-id="995ba-119">Dimensioni di *pszDest*, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="995ba-119">The size of *pszDest*, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="995ba-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="995ba-120">Return value</span></span>

<span data-ttu-id="995ba-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="995ba-121">Type: **int**</span></span>

<span data-ttu-id="995ba-122">Se *pszDest* è **null** o *cchDest* è zero, restituisce la dimensione del buffer, in caratteri, necessaria per contenere una copia con terminazione null della stringa a cui punta *pszSource*.</span><span class="sxs-lookup"><span data-stu-id="995ba-122">If *pszDest* is **NULL** or *cchDest* is zero, returns the size of the buffer, in characters, needed to contain a null-terminated copy of the string pointed to by *pszSource*.</span></span>

<span data-ttu-id="995ba-123">Se *pszDest* è diverso da **null**, restituisce il numero di caratteri copiati correttamente, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="995ba-123">If *pszDest* is non-**NULL**, returns the number of characters successfully copied, including the terminating null character.</span></span>

<span data-ttu-id="995ba-124">Se *pszDest* non è in grado di mantenere l'intera stringa a cui punta *pszSource*, vengono copiati i caratteri (*cchDest*-1), la stringa con terminazione null e *cchDest* restituito.</span><span class="sxs-lookup"><span data-stu-id="995ba-124">If *pszDest* cannot hold the entire string pointed to by *pszSource*, then (*cchDest*-1) characters are copied, the string null-terminated, and *cchDest* returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="995ba-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="995ba-125">Remarks</span></span>

<span data-ttu-id="995ba-126">**Str \_ GetPtr** è disponibile come versione ANSI (**Str \_ GetPtrA**) e Unicode (**Str \_ GetPtrW**).</span><span class="sxs-lookup"><span data-stu-id="995ba-126">**Str\_GetPtr** is available as ANSI (**Str\_GetPtrA**) and Unicode (**Str\_GetPtrW**) versions.</span></span> <span data-ttu-id="995ba-127">Queste funzioni non vengono esportate in base al nome o dichiarate in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="995ba-127">These functions are not exported by name or declared in a public header file.</span></span> <span data-ttu-id="995ba-128">Per usarli, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere il numero ordinale 233 (**Str \_ GetPtrA**) o 235 (**Str \_ GetPtrW**) da ComCtl32.dll per ottenere un puntatore a funzione.</span><span class="sxs-lookup"><span data-stu-id="995ba-128">To use them, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 233 (**Str\_GetPtrA**) or 235 (**Str\_GetPtrW**) from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="995ba-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="995ba-129">Requirements</span></span>



| <span data-ttu-id="995ba-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="995ba-130">Requirement</span></span> | <span data-ttu-id="995ba-131">Valore</span><span class="sxs-lookup"><span data-stu-id="995ba-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="995ba-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="995ba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="995ba-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="995ba-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="995ba-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="995ba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="995ba-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="995ba-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="995ba-136">DLL</span><span class="sxs-lookup"><span data-stu-id="995ba-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="995ba-137"><dt>ComCtl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="995ba-137"><dt>ComCtl32.dll</dt></span></span> </dl> |
| <span data-ttu-id="995ba-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="995ba-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="995ba-139">**Str \_ GetPtrW** (Unicode) e **Str \_ GetPtrA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="995ba-139">**Str\_GetPtrW** (Unicode) and **Str\_GetPtrA** (ANSI)</span></span><br/>                       |



 

