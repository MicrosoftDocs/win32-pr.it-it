---
description: Recupera il tipo e i dati per il valore del registro di sistema specificato in un hive del registro di sistema offline.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Funzione ORGetValue (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328367"
---
# <a name="orgetvalue-function"></a><span data-ttu-id="5bbee-103">ORGetValue (funzione)</span><span class="sxs-lookup"><span data-stu-id="5bbee-103">ORGetValue function</span></span>

<span data-ttu-id="5bbee-104">Recupera il tipo e i dati per il valore del registro di sistema specificato in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="5bbee-104">Retrieves the type and data for the specified registry value in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bbee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bbee-105">Syntax</span></span>


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="5bbee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bbee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbee-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bbee-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbee-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="5bbee-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="5bbee-109">*lpSubKey* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5bbee-109">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbee-110">Nome della chiave del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bbee-110">The name of the registry key.</span></span> <span data-ttu-id="5bbee-111">Questa chiave deve essere una sottochiave della chiave specificata dal parametro *handle* .</span><span class="sxs-lookup"><span data-stu-id="5bbee-111">This key must be a subkey of the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="5bbee-112">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5bbee-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="5bbee-113">Per i nomi di chiave non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="5bbee-113">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="5bbee-114">*lpValue* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5bbee-114">*lpValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbee-115">Nome del valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bbee-115">The name of the registry value.</span></span> <span data-ttu-id="5bbee-116">Se questo parametro è **null** o una stringa vuota, "", la funzione recupera il tipo e i dati per il valore predefinito o senza nome della chiave, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="5bbee-116">If this parameter is **NULL** or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any.</span></span> <span data-ttu-id="5bbee-117">Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="5bbee-117">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="5bbee-118">Le chiavi non dispongono automaticamente di un valore senza nome o predefinito.</span><span class="sxs-lookup"><span data-stu-id="5bbee-118">Keys do not automatically have an unnamed or default value.</span></span> <span data-ttu-id="5bbee-119">I valori senza nome possono essere di qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="5bbee-119">Unnamed values can be of any type.</span></span>

<span data-ttu-id="5bbee-120">Per i nomi di valore non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="5bbee-120">Value names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="5bbee-121">*pdwType* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5bbee-121">*pdwType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbee-122">Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="5bbee-122">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="5bbee-123">Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="5bbee-123">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="5bbee-124">Questo parametro può essere **null** se il tipo non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5bbee-124">This parameter can be **NULL** if the type is not required.</span></span>

</dd> <dt>

<span data-ttu-id="5bbee-125">*pvData* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5bbee-125">*pvData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbee-126">Puntatore a un buffer che riceve i dati del valore.</span><span class="sxs-lookup"><span data-stu-id="5bbee-126">A pointer to a buffer that receives the value's data.</span></span> <span data-ttu-id="5bbee-127">Questo parametro può essere **null** se i dati non sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="5bbee-127">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="5bbee-128">Se i dati sono di tipo stringa, la funzione verifica la presenza di un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="5bbee-128">If the data is a string, the function checks for a terminating null character.</span></span> <span data-ttu-id="5bbee-129">Se non viene trovato, la stringa viene archiviata con un terminatore null se il buffer è sufficientemente grande da contenere il carattere aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="5bbee-129">If one is not found, the string is stored with a null terminator if the buffer is large enough to accommodate the extra character.</span></span> <span data-ttu-id="5bbee-130">In caso contrario, la funzione ha esito negativo e restituisce l'errore \_ più \_ dati.</span><span class="sxs-lookup"><span data-stu-id="5bbee-130">Otherwise, the function fails and returns ERROR\_MORE\_DATA.</span></span>

</dd> <dt>

<span data-ttu-id="5bbee-131">*pcbData* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5bbee-131">*pcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5bbee-132">Puntatore a una variabile che specifica le dimensioni in byte del buffer a cui punta il parametro *pvData* .</span><span class="sxs-lookup"><span data-stu-id="5bbee-132">A pointer to a variable that specifies the size of the buffer pointed to by the *pvData* parameter, in bytes.</span></span> <span data-ttu-id="5bbee-133">Quando la funzione restituisce, questa variabile contiene le dimensioni dei dati copiati in *pvData*.</span><span class="sxs-lookup"><span data-stu-id="5bbee-133">When the function returns, this variable contains the size of the data copied to *pvData*.</span></span>

<span data-ttu-id="5bbee-134">Il parametro *pcbData* può essere **null** solo se *pvData* è **null**.</span><span class="sxs-lookup"><span data-stu-id="5bbee-134">The *pcbData* parameter can be **NULL** only if *pvData* is **NULL**.</span></span>

<span data-ttu-id="5bbee-135">Se i dati sono di \_ tipo reg SZ, \_ reg \_ multisz o reg \_ expand \_ SZ, questa dimensione include i caratteri null o i caratteri di terminazione.</span><span class="sxs-lookup"><span data-stu-id="5bbee-135">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="5bbee-136">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5bbee-136">For more information, see Remarks.</span></span>

<span data-ttu-id="5bbee-137">Se il buffer specificato dal parametro *pvData* non è sufficientemente grande da consentire l'archiviazione dei dati, la funzione restituisce \_ più dati di errore \_ e archivia le dimensioni del buffer richieste nella variabile a cui punta *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="5bbee-137">If the buffer specified by *pvData* parameter is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="5bbee-138">In questo caso, il contenuto del buffer *pvData* non è definito.</span><span class="sxs-lookup"><span data-stu-id="5bbee-138">In this case, the contents of the *pvData* buffer are undefined.</span></span>

<span data-ttu-id="5bbee-139">Se *pvData* è **null** e *pcbData* è diverso da **null**, la funzione restituisce Error \_ Success e archivia le dimensioni dei dati, in byte, nella variabile a cui punta *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="5bbee-139">If *pvData* is **NULL**, and *pcbData* is non-**NULL**, the function returns ERROR\_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="5bbee-140">Questo consente a un'applicazione di determinare il modo migliore per allocare un buffer per i dati del valore.</span><span class="sxs-lookup"><span data-stu-id="5bbee-140">This enables an application to determine the best way to allocate a buffer for the value's data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bbee-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bbee-141">Return value</span></span>

<span data-ttu-id="5bbee-142">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5bbee-142">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5bbee-143">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="5bbee-143">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="5bbee-144">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="5bbee-144">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bbee-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bbee-145">Remarks</span></span>

<span data-ttu-id="5bbee-146">Un'applicazione in genere chiama la funzione [**OREnumValue**](orenumvalue.md) per determinare i nomi dei valori e quindi chiama la funzione **ORGetValue** per recuperare i dati per i nomi.</span><span class="sxs-lookup"><span data-stu-id="5bbee-146">An application typically calls the [**OREnumValue**](orenumvalue.md) function to determine the value names and then calls the **ORGetValue** function to retrieve the data for the names.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bbee-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bbee-147">Requirements</span></span>



| <span data-ttu-id="5bbee-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bbee-148">Requirement</span></span> | <span data-ttu-id="5bbee-149">Valore</span><span class="sxs-lookup"><span data-stu-id="5bbee-149">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbee-150">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5bbee-150">Redistributable</span></span><br/> | <span data-ttu-id="5bbee-151">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="5bbee-151">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="5bbee-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bbee-152">Header</span></span><br/>          | <dl> <span data-ttu-id="5bbee-153"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bbee-153"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="5bbee-154">DLL</span><span class="sxs-lookup"><span data-stu-id="5bbee-154">DLL</span></span><br/>             | <dl> <span data-ttu-id="5bbee-155"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bbee-155"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bbee-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bbee-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbee-157">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="5bbee-157">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="5bbee-158">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="5bbee-158">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="5bbee-159">**OREnumValue**</span><span class="sxs-lookup"><span data-stu-id="5bbee-159">**OREnumValue**</span></span>](orenumvalue.md)
</dt> <dt>

[<span data-ttu-id="5bbee-160">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="5bbee-160">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="5bbee-161">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="5bbee-161">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
