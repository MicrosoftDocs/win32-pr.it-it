---
description: Elimina una sottochiave e i relativi valori da un hive del registro di sistema offline.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Funzione ORDeleteKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331954"
---
# <a name="ordeletekey-function"></a><span data-ttu-id="89872-103">ORDeleteKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="89872-103">ORDeleteKey function</span></span>

<span data-ttu-id="89872-104">Elimina una sottochiave e i relativi valori da un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="89872-104">Deletes a subkey and its values from an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="89872-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89872-105">Syntax</span></span>


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a><span data-ttu-id="89872-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89872-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89872-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89872-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89872-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="89872-108">A handle to an open registry key in an offline registry hive.</span></span> <span data-ttu-id="89872-109">Questo handle viene restituito dalla funzione [**ORCreateKey**](orcreatekey.md) o [**OROpenKey**](oropenkey.md) .</span><span class="sxs-lookup"><span data-stu-id="89872-109">This handle is returned by the [**ORCreateKey**](orcreatekey.md) or [**OROpenKey**](oropenkey.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="89872-110">*lpSubKey* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="89872-110">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89872-111">Nome della chiave da eliminare.</span><span class="sxs-lookup"><span data-stu-id="89872-111">The name of the key to be deleted.</span></span> <span data-ttu-id="89872-112">Deve essere una sottochiave della chiave che *gestisce* gli identificatori, ma non può avere sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="89872-112">It must be a subkey of the key that *Handle* identifies, but it cannot have subkeys.</span></span>

<span data-ttu-id="89872-113">Se la sottochiave non esiste, la funzione restituisce un errore \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="89872-113">If the subkey does not exist, the function returns ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="89872-114">Se questo parametro è **null**, la funzione Elimina la chiave specificata dal parametro *handle* .</span><span class="sxs-lookup"><span data-stu-id="89872-114">If this parameter is **NULL**, the function deletes the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="89872-115">Se la chiave specificata dal parametro *handle* è la chiave radice dell'hive, la funzione restituisce un parametro di errore \_ non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="89872-115">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="89872-116">Per i nomi di chiave non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="89872-116">Key names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89872-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89872-117">Return value</span></span>

<span data-ttu-id="89872-118">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="89872-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="89872-119">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="89872-119">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="89872-120">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="89872-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="89872-121">I codici di errore possibili includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="89872-121">Possible error codes include the following:</span></span>

-   <span data-ttu-id="89872-122">Se la sottochiave specificata non esiste, la funzione restituisce il \_ file di errore \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="89872-122">If the specified subkey does not exist, the function returns ERROR\_FILE\_NOT\_FOUND.</span></span>
-   <span data-ttu-id="89872-123">Se la sottochiave specificata è la chiave radice dell'hive del registro di sistema, la funzione restituisce l'errore \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="89872-123">If the specified subkey is the root key of the registry hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>
-   <span data-ttu-id="89872-124">Se la sottochiave specificata include sottochiavi, la funzione restituisce la chiave di errore \_ \_ con \_ elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="89872-124">If the specified subkey has subkeys, the function returns ERROR\_KEY\_HAS\_CHILDREN.</span></span>

## <a name="remarks"></a><span data-ttu-id="89872-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="89872-125">Remarks</span></span>

<span data-ttu-id="89872-126">Se la chiave del registro di sistema specificata esiste, viene contrassegnata come eliminata.</span><span class="sxs-lookup"><span data-stu-id="89872-126">If the specified registry key exists, it is marked as deleted.</span></span> <span data-ttu-id="89872-127">Una chiave eliminata non viene rimossa fino a quando non viene chiuso l'ultimo handle.</span><span class="sxs-lookup"><span data-stu-id="89872-127">A deleted key is not removed until the last handle to it is closed.</span></span>

<span data-ttu-id="89872-128">La chiave da eliminare non deve contenere sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="89872-128">The key to be deleted must not have subkeys.</span></span> <span data-ttu-id="89872-129">Per eliminare una chiave e tutte le relative sottochiavi, utilizzare la funzione [**OREnumKey**](orenumkey.md) per enumerare le sottochiavi ed eliminarle singolarmente.</span><span class="sxs-lookup"><span data-stu-id="89872-129">To delete a key and all its subkeys, use the [**OREnumKey**](orenumkey.md) function to enumerate the subkeys and delete them individually.</span></span>

<span data-ttu-id="89872-130">È possibile chiamare solo la funzione [**ORCloseKey**](orclosekey.md) su una chiave eliminata. tutte le altre operazioni del registro di sistema offline non riescono</span><span class="sxs-lookup"><span data-stu-id="89872-130">Only the [**ORCloseKey**](orclosekey.md) function may be called on a deleted key; all other offline registry operations fail.</span></span> <span data-ttu-id="89872-131">Se la chiave eliminata è stata creata in modo esplicito chiamando [**ORCreateKey**](orcreatekey.md), le risorse associate alla chiave vengono rilasciate quando viene chiuso l'ultimo handle per la chiave eliminata.</span><span class="sxs-lookup"><span data-stu-id="89872-131">If the deleted key was explicitly created by calling [**ORCreateKey**](orcreatekey.md), resources associated with the key are released when the last handle to the deleted key is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="89872-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89872-132">Requirements</span></span>



| <span data-ttu-id="89872-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="89872-133">Requirement</span></span> | <span data-ttu-id="89872-134">Valore</span><span class="sxs-lookup"><span data-stu-id="89872-134">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89872-135">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="89872-135">Redistributable</span></span><br/> | <span data-ttu-id="89872-136">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="89872-136">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="89872-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89872-137">Header</span></span><br/>          | <dl> <span data-ttu-id="89872-138"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="89872-138"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="89872-139">DLL</span><span class="sxs-lookup"><span data-stu-id="89872-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="89872-140"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89872-140"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89872-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89872-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89872-142">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="89872-142">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="89872-143">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="89872-143">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="89872-144">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="89872-144">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="89872-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="89872-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
