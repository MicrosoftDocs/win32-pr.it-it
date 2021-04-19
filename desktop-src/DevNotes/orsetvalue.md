---
description: Imposta i dati per il valore di una chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Funzione ORSetValue (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332594"
---
# <a name="orsetvalue-function"></a><span data-ttu-id="a7718-103">ORSetValue (funzione)</span><span class="sxs-lookup"><span data-stu-id="a7718-103">ORSetValue function</span></span>

<span data-ttu-id="a7718-104">Imposta i dati per il valore di una chiave del registro di sistema specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a7718-104">Sets the data for the value of a specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7718-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7718-105">Syntax</span></span>


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="a7718-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7718-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7718-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7718-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7718-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a7718-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="a7718-109">*lpValueName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a7718-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7718-110">Nome del valore da impostare.</span><span class="sxs-lookup"><span data-stu-id="a7718-110">The name of the value to be set.</span></span> <span data-ttu-id="a7718-111">Se un valore con questo nome non è già presente nella chiave, la funzione lo aggiunge alla chiave.</span><span class="sxs-lookup"><span data-stu-id="a7718-111">If a value with this name is not already present in the key, the function adds it to the key.</span></span>

<span data-ttu-id="a7718-112">Se *lpValueName* è **null** o una stringa vuota, "", la funzione imposta il tipo e i dati per il valore predefinito o senza nome della chiave.</span><span class="sxs-lookup"><span data-stu-id="a7718-112">If *lpValueName* is **NULL** or an empty string, "", the function sets the type and data for the key's unnamed or default value.</span></span>

<span data-ttu-id="a7718-113">Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="a7718-113">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="a7718-114">Le chiavi del registro di sistema non hanno valori predefiniti, ma possono avere un valore senza nome, che può essere di qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="a7718-114">Registry keys do not have default values, but they can have one unnamed value, which can be of any type.</span></span>

</dd> <dt>

<span data-ttu-id="a7718-115">*dwType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7718-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7718-116">Tipo di dati a cui punta il parametro *lpData* .</span><span class="sxs-lookup"><span data-stu-id="a7718-116">The type of data pointed to by the *lpData* parameter.</span></span> <span data-ttu-id="a7718-117">Per un elenco dei tipi possibili, vedere [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="a7718-117">For a list of the possible types, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7718-118">*lpData* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a7718-118">*lpData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7718-119">Dati da archiviare.</span><span class="sxs-lookup"><span data-stu-id="a7718-119">The data to be stored.</span></span>

<span data-ttu-id="a7718-120">Per i tipi basati su stringa, ad esempio REG \_ SZ, la stringa deve essere con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="a7718-120">For string-based types, such as REG\_SZ, the string must be null-terminated.</span></span> <span data-ttu-id="a7718-121">Per il \_ tipo di \_ dati reg multisz, la stringa deve terminare con due caratteri null.</span><span class="sxs-lookup"><span data-stu-id="a7718-121">For the REG\_MULTI\_SZ data type, the string must be terminated with two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="a7718-122">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7718-122">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7718-123">Dimensioni in byte delle informazioni a cui punta il parametro *lpData* .</span><span class="sxs-lookup"><span data-stu-id="a7718-123">The size of the information pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="a7718-124">Se i dati sono di tipo REG \_ SZ, reg \_ expand \_ sz o reg \_ \_ multisz, *cbData* deve includere la dimensione del carattere null di terminazione o caratteri.</span><span class="sxs-lookup"><span data-stu-id="a7718-124">If the data is of type REG\_SZ, REG\_EXPAND\_SZ, or REG\_MULTI\_SZ, *cbData* must include the size of the terminating null character or characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7718-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7718-125">Return value</span></span>

<span data-ttu-id="a7718-126">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a7718-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a7718-127">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a7718-127">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="a7718-128">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="a7718-128">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7718-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7718-129">Remarks</span></span>

<span data-ttu-id="a7718-130">Le dimensioni dei valori sono limitate dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="a7718-130">Value sizes are limited by available memory.</span></span> <span data-ttu-id="a7718-131">I valori Long (più di 2048 byte) devono essere archiviati come file con i nomi di file archiviati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a7718-131">Long values (more than 2048 bytes) should be stored as files with the file names stored in the registry.</span></span> <span data-ttu-id="a7718-132">Ciò consente di eseguire in modo efficiente il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a7718-132">This helps the registry perform efficiently.</span></span> <span data-ttu-id="a7718-133">Gli elementi dell'applicazione quali le icone, le bitmap e i file eseguibili devono essere archiviati come file e non devono essere inseriti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a7718-133">Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7718-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7718-134">Requirements</span></span>



| <span data-ttu-id="a7718-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7718-135">Requirement</span></span> | <span data-ttu-id="a7718-136">Valore</span><span class="sxs-lookup"><span data-stu-id="a7718-136">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7718-137">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a7718-137">Redistributable</span></span><br/> | <span data-ttu-id="a7718-138">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a7718-138">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="a7718-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7718-139">Header</span></span><br/>          | <dl> <span data-ttu-id="a7718-140"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7718-140"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7718-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a7718-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="a7718-142"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7718-142"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7718-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7718-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7718-144">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="a7718-144">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="a7718-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="a7718-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
