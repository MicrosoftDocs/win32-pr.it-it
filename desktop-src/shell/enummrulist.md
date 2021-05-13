---
description: Enumera il contenuto dell'elenco degli elementi usati più di recente. Recupera facoltativamente un elemento dall'enumerazione .
title: Funzione EnumMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 1e6e4bd0820d35fec2a108a81eb1030567493e6a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843162"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="a915e-104">Funzione EnumMRUListW</span><span class="sxs-lookup"><span data-stu-id="a915e-104">EnumMRUListW function</span></span>

<span data-ttu-id="a915e-105">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a915e-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="a915e-106">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="a915e-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="a915e-107">\]</span><span class="sxs-lookup"><span data-stu-id="a915e-107">\]</span></span>

<span data-ttu-id="a915e-108">Enumera il contenuto dell'elenco degli elementi usati più di recente.</span><span class="sxs-lookup"><span data-stu-id="a915e-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="a915e-109">Recupera facoltativamente un elemento dall'enumerazione .</span><span class="sxs-lookup"><span data-stu-id="a915e-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="a915e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a915e-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="a915e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a915e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a915e-112">*hMRU* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a915e-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a915e-113">Tipo: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="a915e-113">Type: **HANDLE**</span></span>

<span data-ttu-id="a915e-114">Handle dell'elenco MRU, ottenuto al momento della creazione dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a915e-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="a915e-115">*nItem* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a915e-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a915e-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="a915e-116">Type: **int**</span></span>

<span data-ttu-id="a915e-117">Elemento da restituire.</span><span class="sxs-lookup"><span data-stu-id="a915e-117">The item to return.</span></span> <span data-ttu-id="a915e-118">Se questo valore è minore di 0, la funzione restituisce il numero di elementi nell'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="a915e-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="a915e-119">*lpData* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="a915e-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a915e-120">Tipo: **\* void**</span><span class="sxs-lookup"><span data-stu-id="a915e-120">Type: **void\***</span></span>

<span data-ttu-id="a915e-121">Puntatore a un buffer che riceve l'elemento richiesto in *nItem.*</span><span class="sxs-lookup"><span data-stu-id="a915e-121">A pointer to a buffer that receives the item requested in *nItem*.</span></span> <span data-ttu-id="a915e-122">Se *nItem* è minore di 0, il contenuto di questo buffer rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="a915e-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="a915e-123">*uLen* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a915e-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a915e-124">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="a915e-124">Type: **UINT**</span></span>

<span data-ttu-id="a915e-125">Dimensione del buffer, incluso il carattere Null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="a915e-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="a915e-126">Se l'elenco MRU è stato creato con il flag **\_ BINARY MRU,** questa è la dimensione in byte.</span><span class="sxs-lookup"><span data-stu-id="a915e-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="a915e-127">In caso contrario, è la dimensione in caratteri.</span><span class="sxs-lookup"><span data-stu-id="a915e-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a915e-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a915e-128">Return value</span></span>

<span data-ttu-id="a915e-129">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="a915e-129">Type: **int**</span></span>

<span data-ttu-id="a915e-130">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a915e-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="a915e-131">Restituisce il numero di elementi nell'enumerazione, se *nItem* è minore di 0.</span><span class="sxs-lookup"><span data-stu-id="a915e-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="a915e-132">Restituisce -1 se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="a915e-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="a915e-133">In caso contrario, restituisce le dimensioni della stringa restituita in *lpData*, incluso il carattere Null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="a915e-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="a915e-134">Se l'elenco MRU è stato creato con il flag **\_ BINARY MRU,** questa è la dimensione in byte.</span><span class="sxs-lookup"><span data-stu-id="a915e-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="a915e-135">In caso contrario, è la dimensione in caratteri.</span><span class="sxs-lookup"><span data-stu-id="a915e-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a915e-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="a915e-136">Remarks</span></span>

<span data-ttu-id="a915e-137">Questa funzione non è inclusa in un'intestazione o in una libreria pubblica.</span><span class="sxs-lookup"><span data-stu-id="a915e-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="a915e-138">È possibile accedervi tramite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o estrarlo da comctl32.dll ordinale, ovvero 403 per **EnumMRUListW.**</span><span class="sxs-lookup"><span data-stu-id="a915e-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a915e-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a915e-139">Requirements</span></span>



| <span data-ttu-id="a915e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a915e-140">Requirement</span></span> | <span data-ttu-id="a915e-141">Valore</span><span class="sxs-lookup"><span data-stu-id="a915e-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a915e-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a915e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a915e-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a915e-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a915e-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a915e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a915e-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a915e-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a915e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a915e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a915e-147"><dt>Comctl32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a915e-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="a915e-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a915e-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a915e-149">**EnumMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="a915e-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="a915e-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a915e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a915e-151">**CreateMRUListW**</span><span class="sxs-lookup"><span data-stu-id="a915e-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="a915e-152">**MRUINFO**</span><span class="sxs-lookup"><span data-stu-id="a915e-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
