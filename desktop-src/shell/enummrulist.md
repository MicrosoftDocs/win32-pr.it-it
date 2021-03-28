---
description: Enumera il contenuto dell'elenco degli ultimi elementi usati (MRU). Consente, facoltativamente, di recuperare un elemento dall'enumerazione.
title: EnumMRUListW (funzione)
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
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884393"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="83313-104">EnumMRUListW (funzione)</span><span class="sxs-lookup"><span data-stu-id="83313-104">EnumMRUListW function</span></span>

<span data-ttu-id="83313-105">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="83313-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="83313-106">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="83313-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="83313-107">\]</span><span class="sxs-lookup"><span data-stu-id="83313-107">\]</span></span>

<span data-ttu-id="83313-108">Enumera il contenuto dell'elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="83313-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="83313-109">Consente, facoltativamente, di recuperare un elemento dall'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="83313-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="83313-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83313-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="83313-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="83313-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83313-112">*hMRU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83313-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83313-113">Tipo: **handle**</span><span class="sxs-lookup"><span data-stu-id="83313-113">Type: **HANDLE**</span></span>

<span data-ttu-id="83313-114">Handle dell'elenco MRU, ottenuto quando è stato creato l'elenco.</span><span class="sxs-lookup"><span data-stu-id="83313-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="83313-115">*Niten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83313-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83313-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="83313-116">Type: **int**</span></span>

<span data-ttu-id="83313-117">Elemento da restituire.</span><span class="sxs-lookup"><span data-stu-id="83313-117">The item to return.</span></span> <span data-ttu-id="83313-118">Se questo valore è minore di 0, la funzione restituisce il numero di elementi nell'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="83313-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="83313-119">*lpData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="83313-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83313-120">Tipo: \**void \** _</span><span class="sxs-lookup"><span data-stu-id="83313-120">Type: \**void\** _</span></span>

<span data-ttu-id="83313-121">Puntatore a un buffer che riceve l'elemento richiesto in _nItem \*.</span><span class="sxs-lookup"><span data-stu-id="83313-121">A pointer to a buffer that receives the item requested in _nItem\*.</span></span> <span data-ttu-id="83313-122">Se il numero di *Nite* è minore di 0, il contenuto di questo buffer è invariato.</span><span class="sxs-lookup"><span data-stu-id="83313-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="83313-123">*uLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83313-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83313-124">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="83313-124">Type: **UINT**</span></span>

<span data-ttu-id="83313-125">Dimensioni del buffer, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="83313-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="83313-126">Se l'elenco MRU è stato creato con il flag **\_ binario MRU** , corrisponde alle dimensioni in byte.</span><span class="sxs-lookup"><span data-stu-id="83313-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="83313-127">In caso contrario, è la dimensione in caratteri.</span><span class="sxs-lookup"><span data-stu-id="83313-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83313-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83313-128">Return value</span></span>

<span data-ttu-id="83313-129">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="83313-129">Type: **int**</span></span>

<span data-ttu-id="83313-130">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="83313-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="83313-131">Restituisce il numero di elementi nell'enumerazione, se *nitet* è minore di 0.</span><span class="sxs-lookup"><span data-stu-id="83313-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="83313-132">Restituisce-1 se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="83313-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="83313-133">In caso contrario, restituisce le dimensioni della stringa restituita in *lpData*, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="83313-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="83313-134">Se l'elenco MRU è stato creato con il flag **\_ binario MRU** , corrisponde alle dimensioni in byte.</span><span class="sxs-lookup"><span data-stu-id="83313-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="83313-135">In caso contrario, è la dimensione in caratteri.</span><span class="sxs-lookup"><span data-stu-id="83313-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="83313-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="83313-136">Remarks</span></span>

<span data-ttu-id="83313-137">Questa funzione non è inclusa in un'intestazione o in una libreria pubblica.</span><span class="sxs-lookup"><span data-stu-id="83313-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="83313-138">È possibile accedervi tramite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o estratti da comctl32.dll in base al relativo ordinale, ovvero 403 per **EnumMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="83313-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="83313-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83313-139">Requirements</span></span>



| <span data-ttu-id="83313-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="83313-140">Requirement</span></span> | <span data-ttu-id="83313-141">Valore</span><span class="sxs-lookup"><span data-stu-id="83313-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83313-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83313-142">Minimum supported client</span></span><br/> | <span data-ttu-id="83313-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83313-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83313-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83313-144">Minimum supported server</span></span><br/> | <span data-ttu-id="83313-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83313-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83313-146">DLL</span><span class="sxs-lookup"><span data-stu-id="83313-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83313-147"><dt>Comctl32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="83313-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="83313-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="83313-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="83313-149">**EnumMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="83313-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="83313-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83313-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83313-151">**CreateMRUListW**</span><span class="sxs-lookup"><span data-stu-id="83313-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="83313-152">**MRUINFO**</span><span class="sxs-lookup"><span data-stu-id="83313-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
