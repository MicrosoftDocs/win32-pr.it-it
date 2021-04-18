---
description: Enumera i valori per la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline. La funzione recupera le informazioni per un valore sotto la chiave specificata ogni volta che viene chiamata la funzione.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Funzione OREnumValue (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328369"
---
# <a name="orenumvalue-function"></a><span data-ttu-id="635d2-104">OREnumValue (funzione)</span><span class="sxs-lookup"><span data-stu-id="635d2-104">OREnumValue function</span></span>

<span data-ttu-id="635d2-105">Enumera i valori per la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="635d2-105">Enumerates the values for the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="635d2-106">La funzione recupera le informazioni per un valore sotto la chiave specificata ogni volta che viene chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="635d2-106">The function retrieves information for one value under the specified key each time the function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="635d2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="635d2-107">Syntax</span></span>


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a><span data-ttu-id="635d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="635d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="635d2-109">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="635d2-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635d2-110">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="635d2-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="635d2-111">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="635d2-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635d2-112">Indice del valore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="635d2-112">The index of the value to be retrieved.</span></span> <span data-ttu-id="635d2-113">Questo parametro deve essere zero per la prima chiamata alla funzione e quindi essere incrementato per le chiamate successive.</span><span class="sxs-lookup"><span data-stu-id="635d2-113">This parameter should be zero for the first call to the function and then be incremented for subsequent calls.</span></span>

<span data-ttu-id="635d2-114">Poiché i valori non sono ordinati, qualsiasi nuovo valore avrà un indice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="635d2-114">Because values are not ordered, any new value will have an arbitrary index.</span></span> <span data-ttu-id="635d2-115">Ciò significa che la funzione può restituire valori in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="635d2-115">This means that the function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="635d2-116">*lpValueName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="635d2-116">*lpValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="635d2-117">Puntatore a un buffer che riceve il nome del valore come stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="635d2-117">A pointer to a buffer that receives the name of the value as a null-terminated string.</span></span> <span data-ttu-id="635d2-118">Questo buffer deve essere sufficientemente grande da includere il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="635d2-118">This buffer must be large enough to include the terminating null character.</span></span>

<span data-ttu-id="635d2-119">Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="635d2-119">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="635d2-120">*lpcValueName* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="635d2-120">*lpcValueName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="635d2-121">Puntatore a una variabile che specifica la dimensione del buffer a cui punta il parametro *lpValueName* , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="635d2-121">A pointer to a variable that specifies the size of the buffer pointed to by the *lpValueName* parameter, in characters.</span></span> <span data-ttu-id="635d2-122">Quando la funzione restituisce, la variabile riceve il numero di caratteri archiviati nel buffer, escluso il carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="635d2-122">When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="635d2-123">*lpType* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="635d2-123">*lpType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="635d2-124">Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="635d2-124">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="635d2-125">Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="635d2-125">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="635d2-126">Il parametro *lpType* può essere **null** se il codice di tipo non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="635d2-126">The *lpType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="635d2-127">*lpData* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="635d2-127">*lpData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="635d2-128">Puntatore a un buffer che riceve i dati per la voce del valore.</span><span class="sxs-lookup"><span data-stu-id="635d2-128">A pointer to a buffer that receives the data for the value entry.</span></span> <span data-ttu-id="635d2-129">Questo parametro può essere **null** se i dati non sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="635d2-129">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="635d2-130">Se *lpData* è **null** e *lpcbData* è diverso da **null**, la funzione archivia le dimensioni dei dati, in byte, nella variabile a cui punta *lpcbData*.</span><span class="sxs-lookup"><span data-stu-id="635d2-130">If *lpData* is **NULL** and *lpcbData* is non-**NULL**, the function stores the size of the data, in bytes, in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="635d2-131">Questo consente a un'applicazione di determinare il modo migliore per allocare un buffer per i dati.</span><span class="sxs-lookup"><span data-stu-id="635d2-131">This enables an application to determine the best way to allocate a buffer for the data.</span></span>

</dd> <dt>

<span data-ttu-id="635d2-132">*lpcbData* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="635d2-132">*lpcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="635d2-133">Puntatore a una variabile che specifica le dimensioni in byte del buffer a cui punta il parametro *lpData* .</span><span class="sxs-lookup"><span data-stu-id="635d2-133">A pointer to a variable that specifies the size of the buffer pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="635d2-134">Quando la funzione restituisce, la variabile riceve il numero di byte archiviati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="635d2-134">When the function returns, the variable receives the number of bytes stored in the buffer.</span></span>

<span data-ttu-id="635d2-135">Questo parametro può essere **null** solo se *lpData* è **null**.</span><span class="sxs-lookup"><span data-stu-id="635d2-135">This parameter can be **NULL** only if *lpData* is **NULL**.</span></span>

<span data-ttu-id="635d2-136">Se i dati sono di \_ tipo reg SZ, \_ reg \_ multisz o reg \_ expand \_ SZ, questa dimensione include i caratteri null o i caratteri di terminazione.</span><span class="sxs-lookup"><span data-stu-id="635d2-136">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="635d2-137">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="635d2-137">For more information, see Remarks.</span></span>

<span data-ttu-id="635d2-138">Se il buffer specificato da *lpData* non è sufficientemente grande da consentire l'archiviazione dei dati, la funzione restituisce \_ più dati di errore \_ e archivia le dimensioni del buffer richieste nella variabile a cui punta *lpcbData*.</span><span class="sxs-lookup"><span data-stu-id="635d2-138">If the buffer specified by *lpData* is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="635d2-139">In questo caso, il contenuto di *lpData* non è definito.</span><span class="sxs-lookup"><span data-stu-id="635d2-139">In this case, the contents of *lpData* are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="635d2-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="635d2-140">Return value</span></span>

<span data-ttu-id="635d2-141">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="635d2-141">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="635d2-142">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="635d2-142">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="635d2-143">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="635d2-143">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="635d2-144">Se il buffer *lpData* è troppo piccolo per ricevere il valore, la funzione restituisce un errore di \_ altri \_ dati.</span><span class="sxs-lookup"><span data-stu-id="635d2-144">If the *lpData* buffer is too small to receive the value, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="635d2-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="635d2-145">Remarks</span></span>

<span data-ttu-id="635d2-146">Per enumerare i valori, un'applicazione deve chiamare inizialmente la funzione **OREnumValue** con il parametro *dwIndex* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="635d2-146">To enumerate values, an application should initially call the **OREnumValue** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="635d2-147">L'applicazione deve quindi incrementare *dwIndex* e chiamare la funzione **OREnumValue** fino a quando non sono presenti altri valori (fino a quando la funzione \_ non restituisce \_ più \_ elementi).</span><span class="sxs-lookup"><span data-stu-id="635d2-147">The application should then increment *dwIndex* and call the **OREnumValue** function until there are no more values (until the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="635d2-148">L'applicazione può inoltre impostare *dwIndex* sull'indice dell'ultimo valore nella prima chiamata alla funzione e decrementare l'indice fino a quando non viene enumerato il valore con indice 0.</span><span class="sxs-lookup"><span data-stu-id="635d2-148">The application can also set *dwIndex* to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated.</span></span> <span data-ttu-id="635d2-149">Per recuperare l'indice dell'ultimo valore, utilizzare la funzione [**ORQueryInfoKey**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="635d2-149">To retrieve the index of the last value, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

<span data-ttu-id="635d2-150">Quando si usa **OREnumValue**, un'applicazione non deve chiamare funzioni del registro di sistema offline che potrebbero modificare la chiave sottoposta a query.</span><span class="sxs-lookup"><span data-stu-id="635d2-150">While using **OREnumValue**, an application should not call any offline registry functions that might change the key being queried.</span></span>

<span data-ttu-id="635d2-151">Se i dati sono di \_ tipo reg SZ, \_ reg \_ multisz o reg \_ expand \_ SZ, è possibile che la stringa non sia stata archiviata con i caratteri di terminazione null appropriati.</span><span class="sxs-lookup"><span data-stu-id="635d2-151">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, the string may not have been stored with the proper null-terminating characters.</span></span> <span data-ttu-id="635d2-152">Pertanto, anche se la funzione restituisce un errore di \_ esito positivo, l'applicazione deve garantire che la stringa venga terminata correttamente prima di utilizzarla; in caso contrario, potrebbe sovrascrivere un buffer.</span><span class="sxs-lookup"><span data-stu-id="635d2-152">Therefore, even if the function returns ERROR\_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer.</span></span> <span data-ttu-id="635d2-153">(Si noti che REG \_ Le \_ stringhe a più SZ devono avere due caratteri di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="635d2-153">(Note that REG\_MULTI\_SZ strings should have two null-terminating characters.)</span></span>

<span data-ttu-id="635d2-154">Per determinare la dimensione massima del nome e dei buffer dei dati, utilizzare la funzione [**ORQueryInfoKey**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="635d2-154">To determine the maximum size of the name and data buffers, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="635d2-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="635d2-155">Requirements</span></span>



| <span data-ttu-id="635d2-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="635d2-156">Requirement</span></span> | <span data-ttu-id="635d2-157">Valore</span><span class="sxs-lookup"><span data-stu-id="635d2-157">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="635d2-158">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="635d2-158">Redistributable</span></span><br/> | <span data-ttu-id="635d2-159">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="635d2-159">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="635d2-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="635d2-160">Header</span></span><br/>          | <dl> <span data-ttu-id="635d2-161"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="635d2-161"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="635d2-162">DLL</span><span class="sxs-lookup"><span data-stu-id="635d2-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="635d2-163"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="635d2-163"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="635d2-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="635d2-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="635d2-165">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="635d2-165">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="635d2-166">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="635d2-166">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="635d2-167">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="635d2-167">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="635d2-168">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="635d2-168">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
