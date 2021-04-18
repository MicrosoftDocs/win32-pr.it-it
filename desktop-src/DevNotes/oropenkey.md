---
description: Apre la chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Funzione OROpenKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331465"
---
# <a name="oropenkey-function"></a><span data-ttu-id="3b884-103">OROpenKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="3b884-103">OROpenKey function</span></span>

<span data-ttu-id="3b884-104">Apre la chiave del registro di sistema specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="3b884-104">Opens the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b884-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b884-105">Syntax</span></span>


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="3b884-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b884-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b884-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b884-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="3b884-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="3b884-109">*lpSubKeyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3b884-109">*lpSubKeyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b884-110">Puntatore a una stringa UNICODE che contiene il nome della chiave del registro di sistema da aprire.</span><span class="sxs-lookup"><span data-stu-id="3b884-110">A pointer to a UNICODE string that contains the name of the registry key to be opened.</span></span> <span data-ttu-id="3b884-111">Questa chiave deve essere una sottochiave della chiave identificata dal parametro *handle* .</span><span class="sxs-lookup"><span data-stu-id="3b884-111">This key must be a subkey of the key identified by the *Handle* parameter.</span></span>

<span data-ttu-id="3b884-112">Per i nomi di chiave non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="3b884-112">Key names are not case sensitive.</span></span>

<span data-ttu-id="3b884-113">Se questo parametro è **null** o un puntatore a una stringa vuota, la funzione restituisce lo stesso handle passato.</span><span class="sxs-lookup"><span data-stu-id="3b884-113">If this parameter is **NULL** or a pointer to an empty string, the function returns the same handle that was passed in.</span></span> <span data-ttu-id="3b884-114">Se la chiave specificata dal parametro *handle* è la chiave radice dell'hive, la funzione restituisce un parametro di errore \_ non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="3b884-114">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="3b884-115">Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="3b884-115">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b884-116">*phkResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3b884-116">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b884-117">Puntatore a una variabile che riceve un handle per la chiave aperta.</span><span class="sxs-lookup"><span data-stu-id="3b884-117">A pointer to a variable that receives a handle to the opened key.</span></span> <span data-ttu-id="3b884-118">Usare la funzione [**ORCloseKey**](orclosekey.md) per chiudere la chiave dopo aver terminato di usare l'handle.</span><span class="sxs-lookup"><span data-stu-id="3b884-118">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b884-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b884-119">Return value</span></span>

<span data-ttu-id="3b884-120">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3b884-120">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3b884-121">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="3b884-121">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="3b884-122">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="3b884-122">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="3b884-123">Se l'handle da restituire è un handle per la chiave radice dell'hive, la funzione restituisce l'errore \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="3b884-123">If the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="3b884-124">Se la chiave specificata è stata contrassegnata come eliminata, questa funzione restituisce la chiave di errore \_ \_ eliminata.</span><span class="sxs-lookup"><span data-stu-id="3b884-124">If the specified key has been marked as deleted, this function returns ERROR\_KEY\_DELETED.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b884-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b884-125">Remarks</span></span>

<span data-ttu-id="3b884-126">Non è possibile usare la funzione **OROpenKey** per aprire la chiave radice in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="3b884-126">The **OROpenKey** function cannot be used to open the root key in an offline registry hive.</span></span> <span data-ttu-id="3b884-127">Per ottenere un handle per la chiave radice di un hive, usare la funzione [**OROpenHive**](oropenhive.md) per caricare l'hive in memoria.</span><span class="sxs-lookup"><span data-stu-id="3b884-127">To obtain a handle to the root key of a hive, use the [**OROpenHive**](oropenhive.md) function to load the hive into memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b884-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b884-128">Requirements</span></span>



| <span data-ttu-id="3b884-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b884-129">Requirement</span></span> | <span data-ttu-id="3b884-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3b884-130">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b884-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3b884-131">Redistributable</span></span><br/> | <span data-ttu-id="3b884-132">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="3b884-132">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="3b884-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b884-133">Header</span></span><br/>          | <dl> <span data-ttu-id="3b884-134"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b884-134"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b884-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3b884-135">DLL</span></span><br/>             | <dl> <span data-ttu-id="3b884-136"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b884-136"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b884-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b884-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b884-138">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="3b884-138">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="3b884-139">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="3b884-139">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="3b884-140">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="3b884-140">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="3b884-141">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="3b884-141">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
