---
description: Recupera le informazioni sulla chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Funzione ORQueryInfoKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330426"
---
# <a name="orqueryinfokey-function"></a><span data-ttu-id="e1102-103">ORQueryInfoKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="e1102-103">ORQueryInfoKey function</span></span>

<span data-ttu-id="e1102-104">Recupera le informazioni sulla chiave del registro di sistema specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="e1102-104">Retrieves information about the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1102-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1102-105">Syntax</span></span>


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="e1102-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1102-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1102-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1102-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="e1102-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-109">*lpClass* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-109">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-110">Puntatore a un buffer che riceve la classe chiave.</span><span class="sxs-lookup"><span data-stu-id="e1102-110">A pointer to a buffer that receives the key class.</span></span> <span data-ttu-id="e1102-111">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-112">*lpcClass* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-112">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-113">Puntatore a una variabile che specifica la dimensione del buffer a cui punta il parametro *lpClass* , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="e1102-113">A pointer to a variable that specifies the size of the buffer pointed to by the *lpClass* parameter, in characters.</span></span>

<span data-ttu-id="e1102-114">La dimensione deve includere il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e1102-114">The size should include the terminating null character.</span></span> <span data-ttu-id="e1102-115">Quando la funzione restituisce, questa variabile contiene le dimensioni della stringa di classe archiviata nel buffer.</span><span class="sxs-lookup"><span data-stu-id="e1102-115">When the function returns, this variable contains the size of the class string that is stored in the buffer.</span></span> <span data-ttu-id="e1102-116">Il conteggio restituito non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e1102-116">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="e1102-117">Se il buffer non è sufficientemente grande, la funzione restituisce l'errore \_ più \_ dati e la variabile contiene la dimensione della stringa, in caratteri, senza contare il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e1102-117">If the buffer is not big enough, the function returns ERROR\_MORE\_DATA, and the variable contains the size of the string, in characters, without counting the terminating null character.</span></span>

<span data-ttu-id="e1102-118">Se *lpClass* è **null**, *lpcClass* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e1102-118">If *lpClass* is **NULL**, *lpcClass* can be **NULL**.</span></span>

<span data-ttu-id="e1102-119">Se il parametro *lpClass* è un indirizzo valido, ma il parametro *lpcClass* non è (ad esempio, se il parametro *lpcClass* è **null**), la funzione restituisce l'errore \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="e1102-119">If the *lpClass* parameter is a valid address, but the *lpcClass* parameter is not (for example, if the *lpcClass* parameter is **NULL**) then the function returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-120">*lpcSubKeys* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-120">*lpcSubKeys* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-121">Puntatore a una variabile che riceve il numero di sottochiavi contenute nella chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="e1102-121">A pointer to a variable that receives the number of subkeys that are contained by the specified key.</span></span> <span data-ttu-id="e1102-122">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-123">*lpcMaxSubKeyLen* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-123">*lpcMaxSubKeyLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-124">Puntatore a una variabile che riceve le dimensioni della sottochiave della chiave con il nome più lungo, in caratteri Unicode, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e1102-124">A pointer to a variable that receives the size of the key's subkey with the longest name, in Unicode characters, not including the terminating null character.</span></span> <span data-ttu-id="e1102-125">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-125">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-126">*lpcMaxClassLen* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-126">*lpcMaxClassLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-127">Puntatore a una variabile che riceve la dimensione della stringa più estesa che specifica una classe della sottochiave, in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1102-127">A pointer to a variable that receives the size of the longest string that specifies a subkey class, in Unicode characters.</span></span> <span data-ttu-id="e1102-128">Il conteggio restituito non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e1102-128">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="e1102-129">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-129">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-130">*lpcValues* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-130">*lpcValues* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-131">Puntatore a una variabile che riceve il numero di valori associati alla chiave.</span><span class="sxs-lookup"><span data-stu-id="e1102-131">A pointer to a variable that receives the number of values that are associated with the key.</span></span> <span data-ttu-id="e1102-132">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-132">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-133">*lpcMaxValueNameLen* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-133">*lpcMaxValueNameLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-134">Puntatore a una variabile che riceve le dimensioni del nome più lungo del valore della chiave, in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1102-134">A pointer to a variable that receives the size of the key's longest value name, in Unicode characters.</span></span> <span data-ttu-id="e1102-135">La dimensione non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e1102-135">The size does not include the terminating null character.</span></span> <span data-ttu-id="e1102-136">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-137">*lpcMaxValueLen* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-137">*lpcMaxValueLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-138">Puntatore a una variabile che riceve le dimensioni del componente dati più lungo tra i valori della chiave, in byte.</span><span class="sxs-lookup"><span data-stu-id="e1102-138">A pointer to a variable that receives the size of the longest data component among the key's values, in bytes.</span></span> <span data-ttu-id="e1102-139">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-139">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-140">*lpcbSecurityDescriptor* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-140">*lpcbSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-141">Puntatore a una variabile che riceve le dimensioni in byte del descrittore di sicurezza della chiave.</span><span class="sxs-lookup"><span data-stu-id="e1102-141">A pointer to a variable that receives the size of the key's security descriptor, in bytes.</span></span> <span data-ttu-id="e1102-142">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-142">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1102-143">*lpftLastWriteTime* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e1102-143">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1102-144">Puntatore a una struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che riceve l'ora dell'ultima scrittura.</span><span class="sxs-lookup"><span data-stu-id="e1102-144">A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the last write time.</span></span> <span data-ttu-id="e1102-145">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e1102-145">This parameter can be **NULL**.</span></span>

<span data-ttu-id="e1102-146">La funzione imposta i membri della struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) per indicare l'ultima modifica apportata alla chiave o a una delle relative voci di valore.</span><span class="sxs-lookup"><span data-stu-id="e1102-146">The function sets the members of the [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to indicate the last time that the key or any of its value entries is modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1102-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1102-147">Return value</span></span>

<span data-ttu-id="e1102-148">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e1102-148">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e1102-149">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="e1102-149">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="e1102-150">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="e1102-150">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="e1102-151">Se il buffer *lpClass* è troppo piccolo per ricevere il nome della classe, la funzione restituisce l'errore di \_ altri \_ dati.</span><span class="sxs-lookup"><span data-stu-id="e1102-151">If the *lpClass* buffer is too small to receive the name of the class, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1102-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1102-152">Requirements</span></span>



| <span data-ttu-id="e1102-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1102-153">Requirement</span></span> | <span data-ttu-id="e1102-154">Valore</span><span class="sxs-lookup"><span data-stu-id="e1102-154">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1102-155">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e1102-155">Redistributable</span></span><br/> | <span data-ttu-id="e1102-156">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="e1102-156">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="e1102-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1102-157">Header</span></span><br/>          | <dl> <span data-ttu-id="e1102-158"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1102-158"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1102-159">DLL</span><span class="sxs-lookup"><span data-stu-id="e1102-159">DLL</span></span><br/>             | <dl> <span data-ttu-id="e1102-160"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1102-160"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1102-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1102-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1102-162">FILETIME</span><span class="sxs-lookup"><span data-stu-id="e1102-162">FILETIME</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="e1102-163">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="e1102-163">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="e1102-164">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="e1102-164">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="e1102-165">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="e1102-165">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> </dl>

 

 
