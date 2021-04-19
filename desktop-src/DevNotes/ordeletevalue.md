---
description: Rimuove un valore denominato dalla chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Funzione ORDeleteValue (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331949"
---
# <a name="ordeletevalue-function"></a><span data-ttu-id="38590-103">ORDeleteValue (funzione)</span><span class="sxs-lookup"><span data-stu-id="38590-103">ORDeleteValue function</span></span>

<span data-ttu-id="38590-104">Rimuove un valore denominato dalla chiave del registro di sistema specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="38590-104">Removes a named value from the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="38590-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38590-105">Syntax</span></span>


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a><span data-ttu-id="38590-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="38590-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38590-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38590-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38590-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="38590-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="38590-109">*lpValueName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="38590-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="38590-110">Valore del registro di sistema da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="38590-110">The registry value to be removed.</span></span> <span data-ttu-id="38590-111">Se questo parametro è **null** o una stringa vuota, viene rimosso il valore predefinito senza nome impostato dalla funzione [**ORSetValue**](orsetvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="38590-111">If this parameter is **NULL** or an empty string, the default unnamed value set by the [**ORSetValue**](orsetvalue.md) function is removed.</span></span>

<span data-ttu-id="38590-112">Per i nomi di valore non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="38590-112">Value names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38590-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38590-113">Return value</span></span>

<span data-ttu-id="38590-114">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="38590-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="38590-115">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="38590-115">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="38590-116">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="38590-116">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="38590-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38590-117">Requirements</span></span>



| <span data-ttu-id="38590-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="38590-118">Requirement</span></span> | <span data-ttu-id="38590-119">Valore</span><span class="sxs-lookup"><span data-stu-id="38590-119">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38590-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="38590-120">Redistributable</span></span><br/> | <span data-ttu-id="38590-121">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="38590-121">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="38590-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38590-122">Header</span></span><br/>          | <dl> <span data-ttu-id="38590-123"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="38590-123"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="38590-124">DLL</span><span class="sxs-lookup"><span data-stu-id="38590-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="38590-125"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38590-125"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38590-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38590-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38590-127">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="38590-127">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
