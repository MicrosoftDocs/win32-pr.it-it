---
description: Enumera le sottochiavi della chiave del registro di sistema aperta specificata in un hive del registro di sistema offline. La funzione recupera le informazioni su una sottochiave ogni volta che viene chiamata.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Funzione OREnumKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330864"
---
# <a name="orenumkey-function"></a><span data-ttu-id="a3256-104">OREnumKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="a3256-104">OREnumKey function</span></span>

<span data-ttu-id="a3256-105">Enumera le sottochiavi della chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a3256-105">Enumerates the subkeys of the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="a3256-106">La funzione recupera le informazioni su una sottochiave ogni volta che viene chiamata.</span><span class="sxs-lookup"><span data-stu-id="a3256-106">The function retrieves information about one subkey each time it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3256-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3256-107">Syntax</span></span>


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="a3256-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3256-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3256-109">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3256-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3256-110">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a3256-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="a3256-111">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3256-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3256-112">Indice della sottochiave da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a3256-112">The index of the subkey to retrieve.</span></span> <span data-ttu-id="a3256-113">Questo parametro deve essere zero per la prima chiamata alla funzione e quindi incrementato per le chiamate successive.</span><span class="sxs-lookup"><span data-stu-id="a3256-113">This parameter should be zero for the first call to the function and then incremented for subsequent calls.</span></span>

<span data-ttu-id="a3256-114">Poiché le sottochiavi non sono ordinate, qualsiasi nuova sottochiave avrà un indice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a3256-114">Because subkeys are not ordered, any new subkey will have an arbitrary index.</span></span> <span data-ttu-id="a3256-115">Ciò significa che la funzione può restituire sottochiavi in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="a3256-115">This means that the function may return subkeys in any order.</span></span>

</dd> <dt>

<span data-ttu-id="a3256-116">*lpName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3256-116">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3256-117">Puntatore a un buffer che riceve il nome della sottochiave, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="a3256-117">A pointer to a buffer that receives the name of the subkey, including the terminating null character.</span></span> <span data-ttu-id="a3256-118">La funzione copia nel buffer solo il nome della sottochiave, non la gerarchia di chiavi completa.</span><span class="sxs-lookup"><span data-stu-id="a3256-118">The function copies only the name of the subkey, not the full key hierarchy, to the buffer.</span></span> <span data-ttu-id="a3256-119">Se la funzione ha esito negativo, nessuna informazione viene copiata in questo buffer.</span><span class="sxs-lookup"><span data-stu-id="a3256-119">If the function fails, no information is copied to this buffer.</span></span>

<span data-ttu-id="a3256-120">Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="a3256-120">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3256-121">*lpcName* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a3256-121">*lpcName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3256-122">Puntatore a una variabile che specifica la dimensione del buffer specificato dal parametro *lpName* in **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="a3256-122">A pointer to a variable that specifies the size of the buffer specified by the *lpName* parameter, in **WCHARs**.</span></span> <span data-ttu-id="a3256-123">Questa dimensione deve includere il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="a3256-123">This size should include the terminating null character.</span></span> <span data-ttu-id="a3256-124">Se la funzione ha esito positivo, la variabile a cui punta *lpcName* contiene il numero di caratteri archiviati nel buffer, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="a3256-124">If the function succeeds, the variable pointed to by *lpcName* contains the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="a3256-125">*lpClass* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a3256-125">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a3256-126">Puntatore a un buffer che riceve la stringa di classe con terminazione null della sottochiave enumerata.</span><span class="sxs-lookup"><span data-stu-id="a3256-126">A pointer to a buffer that receives the null-terminated class string of the enumerated subkey.</span></span> <span data-ttu-id="a3256-127">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a3256-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a3256-128">*lpcClass* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a3256-128">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a3256-129">Puntatore a una variabile che specifica la dimensione del buffer specificato dal parametro *lpClass* in **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="a3256-129">A pointer to a variable that specifies the size of the buffer specified by the *lpClass* parameter, in **WCHARs**.</span></span> <span data-ttu-id="a3256-130">La dimensione deve includere il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="a3256-130">The size should include the terminating null character.</span></span> <span data-ttu-id="a3256-131">Se la funzione ha esito positivo, *lpcClass* contiene il numero di caratteri archiviati nel buffer, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="a3256-131">If the function succeeds, *lpcClass* contains the number of characters stored in the buffer, not including the terminating null character.</span></span> <span data-ttu-id="a3256-132">Questo parametro può essere **null** solo se *lpClass* è **null**.</span><span class="sxs-lookup"><span data-stu-id="a3256-132">This parameter can be **NULL** only if *lpClass* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a3256-133">*lpftLastWriteTime* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a3256-133">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a3256-134">Puntatore alla struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che riceve l'ora dell'ultima scrittura della sottochiave enumerata.</span><span class="sxs-lookup"><span data-stu-id="a3256-134">A pointer to [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the time at which the enumerated subkey was last written.</span></span> <span data-ttu-id="a3256-135">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a3256-135">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3256-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3256-136">Return value</span></span>

<span data-ttu-id="a3256-137">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a3256-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a3256-138">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a3256-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="a3256-139">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="a3256-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="a3256-140">I codici di errore possibili includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3256-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="a3256-141">Se il buffer *lpName* è troppo piccolo per ricevere il nome della chiave, la funzione restituisce l'errore di \_ altri \_ dati.</span><span class="sxs-lookup"><span data-stu-id="a3256-141">If the *lpName* buffer is too small to receive the name of the key, the function returns ERROR\_MORE\_DATA.</span></span>
-   <span data-ttu-id="a3256-142">Se non sono disponibili altre sottochiavi, la funzione restituisce l'errore \_ non \_ più \_ elementi.</span><span class="sxs-lookup"><span data-stu-id="a3256-142">If there are no more subkeys available, the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3256-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3256-143">Remarks</span></span>

<span data-ttu-id="a3256-144">Per enumerare le sottochiavi, un'applicazione deve chiamare inizialmente la funzione **OREnumKey** con il parametro *dwIndex* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a3256-144">To enumerate subkeys, an application should initially call the **OREnumKey** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="a3256-145">L'applicazione deve quindi incrementare il parametro *dwIndex* e chiamare **OREnumKey** fino a quando non sono presenti altre sottochiavi, ovvero la funzione restituisce \_ un errore non \_ più \_ elementi.</span><span class="sxs-lookup"><span data-stu-id="a3256-145">The application should then increment the *dwIndex* parameter and call **OREnumKey** until there are no more subkeys (meaning the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="a3256-146">L'applicazione può anche impostare *dwIndex* sull'indice dell'ultima sottochiave nella prima chiamata alla funzione e decrementare l'indice fino a quando non viene enumerata la sottochiave con indice 0.</span><span class="sxs-lookup"><span data-stu-id="a3256-146">The application can also set *dwIndex* to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated.</span></span> <span data-ttu-id="a3256-147">Per recuperare l'indice dell'ultima sottochiave, usare la funzione [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .</span><span class="sxs-lookup"><span data-stu-id="a3256-147">To retrieve the index of the last subkey, use the [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) function.</span></span>

<span data-ttu-id="a3256-148">Mentre un'applicazione utilizza la funzione **OREnumKey** , non deve effettuare chiamate a funzioni del registro di sistema non in linea che potrebbero modificare la chiave enumerata.</span><span class="sxs-lookup"><span data-stu-id="a3256-148">While an application is using the **OREnumKey** function, it should not make calls to any offline registry functions that might change the key being enumerated.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3256-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3256-149">Requirements</span></span>



| <span data-ttu-id="a3256-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3256-150">Requirement</span></span> | <span data-ttu-id="a3256-151">Valore</span><span class="sxs-lookup"><span data-stu-id="a3256-151">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3256-152">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a3256-152">Redistributable</span></span><br/> | <span data-ttu-id="a3256-153">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a3256-153">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="a3256-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3256-154">Header</span></span><br/>          | <dl> <span data-ttu-id="a3256-155"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3256-155"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3256-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a3256-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="a3256-157"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3256-157"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3256-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3256-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3256-159">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="a3256-159">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="a3256-160">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="a3256-160">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="a3256-161">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="a3256-161">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="a3256-162">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="a3256-162">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
