---
description: Chiude l'hive del registro di sistema offline specificato e libera la memoria allocata per l'hive.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Funzione ORCloseHive (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331960"
---
# <a name="orclosehive-function"></a><span data-ttu-id="4f34a-103">ORCloseHive (funzione)</span><span class="sxs-lookup"><span data-stu-id="4f34a-103">ORCloseHive function</span></span>

<span data-ttu-id="4f34a-104">Chiude l'hive del registro di sistema offline specificato e libera la memoria allocata per l'hive.</span><span class="sxs-lookup"><span data-stu-id="4f34a-104">Closes the specified offline registry hive and frees memory allocated for the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f34a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f34a-105">Syntax</span></span>


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="4f34a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f34a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f34a-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f34a-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f34a-108">Handle per la chiave radice dell'hive del registro di sistema offline da chiudere.</span><span class="sxs-lookup"><span data-stu-id="4f34a-108">A handle to the root key of the offline registry hive to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f34a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f34a-109">Return value</span></span>

<span data-ttu-id="4f34a-110">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4f34a-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="4f34a-111">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="4f34a-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="4f34a-112">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="4f34a-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f34a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f34a-113">Remarks</span></span>

<span data-ttu-id="4f34a-114">La funzione **ORCloseHive** libera tutta la memoria allocata dalle funzioni del registro di sistema offline per conto dell'hive specificato.</span><span class="sxs-lookup"><span data-stu-id="4f34a-114">The **ORCloseHive** function frees all memory allocated by the offline registry functions on behalf of the specified hive.</span></span>

<span data-ttu-id="4f34a-115">Per mantenere le modifiche apportate all'hive, chiamare la funzione [**ORSaveHive**](orsavehive.md) prima di chiamare **ORCloseHive**.</span><span class="sxs-lookup"><span data-stu-id="4f34a-115">To preserve changes to the hive, call the [**ORSaveHive**](orsavehive.md) function before calling **ORCloseHive**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f34a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f34a-116">Requirements</span></span>



| <span data-ttu-id="4f34a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f34a-117">Requirement</span></span> | <span data-ttu-id="4f34a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4f34a-118">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f34a-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4f34a-119">Redistributable</span></span><br/> | <span data-ttu-id="4f34a-120">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="4f34a-120">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="4f34a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f34a-121">Header</span></span><br/>          | <dl> <span data-ttu-id="4f34a-122"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f34a-122"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f34a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4f34a-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="4f34a-124"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f34a-124"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f34a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f34a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f34a-126">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="4f34a-126">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="4f34a-127">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="4f34a-127">**ORSaveHive**</span></span>](orsavehive.md)
</dt> </dl>

 

 
