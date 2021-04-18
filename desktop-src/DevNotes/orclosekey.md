---
description: Chiude un handle per la chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: Funzione ORCloseKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331959"
---
# <a name="orclosekey-function"></a><span data-ttu-id="86e0d-103">ORCloseKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="86e0d-103">ORCloseKey function</span></span>

<span data-ttu-id="86e0d-104">Chiude un handle per la chiave del registro di sistema specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="86e0d-104">Closes a handle to the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e0d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86e0d-105">Syntax</span></span>


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="86e0d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86e0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e0d-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86e0d-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e0d-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="86e0d-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e0d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86e0d-109">Return value</span></span>

<span data-ttu-id="86e0d-110">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="86e0d-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="86e0d-111">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="86e0d-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="86e0d-112">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="86e0d-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="86e0d-113">Se la chiave specificata è la chiave radice dell'hive del registro di sistema, la funzione ha esito negativo con errore \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="86e0d-113">If the specified key is the root key of the registry hive, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e0d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="86e0d-114">Remarks</span></span>

<span data-ttu-id="86e0d-115">L'handle per una chiave specificata non deve essere usato dopo la chiusura, perché non sarà più valido.</span><span class="sxs-lookup"><span data-stu-id="86e0d-115">The handle for a specified key should not be used after it has been closed, because it will no longer be valid.</span></span> <span data-ttu-id="86e0d-116">Gli handle di chiave non devono essere lasciati aperti più a lungo del necessario.</span><span class="sxs-lookup"><span data-stu-id="86e0d-116">Key handles should not be left open any longer than necessary.</span></span>

<span data-ttu-id="86e0d-117">Usare la funzione [**ORCloseHive**](orclosehive.md) per chiudere un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="86e0d-117">Use the [**ORCloseHive**](orclosehive.md) function to close an offline registry hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e0d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86e0d-118">Requirements</span></span>



| <span data-ttu-id="86e0d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86e0d-119">Requirement</span></span> | <span data-ttu-id="86e0d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="86e0d-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86e0d-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="86e0d-121">Redistributable</span></span><br/> | <span data-ttu-id="86e0d-122">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="86e0d-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="86e0d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86e0d-123">Header</span></span><br/>          | <dl> <span data-ttu-id="86e0d-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="86e0d-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="86e0d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="86e0d-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="86e0d-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e0d-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e0d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86e0d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e0d-128">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="86e0d-128">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="86e0d-129">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="86e0d-129">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="86e0d-130">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="86e0d-130">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="86e0d-131">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="86e0d-131">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
