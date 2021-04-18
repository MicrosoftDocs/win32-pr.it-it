---
description: Crea un hive del registro di sistema offline che contiene una singola chiave radice vuota.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Funzione ORCreateHive (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331958"
---
# <a name="orcreatehive-function"></a><span data-ttu-id="86dbb-103">ORCreateHive (funzione)</span><span class="sxs-lookup"><span data-stu-id="86dbb-103">ORCreateHive function</span></span>

<span data-ttu-id="86dbb-104">Crea un hive del registro di sistema offline che contiene una singola chiave radice vuota.</span><span class="sxs-lookup"><span data-stu-id="86dbb-104">Creates an offline registry hive that contains a single empty root key.</span></span>

## <a name="syntax"></a><span data-ttu-id="86dbb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86dbb-105">Syntax</span></span>


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="86dbb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86dbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86dbb-107">*phkResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86dbb-107">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86dbb-108">Punta a una variabile per ricevere un handle per la chiave radice dell'hive del registro di sistema offline appena creato.</span><span class="sxs-lookup"><span data-stu-id="86dbb-108">Points to a variable to receive a handle to the root key of the newly created offline registry hive.</span></span> <span data-ttu-id="86dbb-109">Se non è possibile creare l'hive, la funzione imposta questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="86dbb-109">If the hive cannot be created, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86dbb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86dbb-110">Return value</span></span>

<span data-ttu-id="86dbb-111">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="86dbb-111">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="86dbb-112">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="86dbb-112">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="86dbb-113">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="86dbb-113">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="86dbb-114">Se la memoria disponibile non è sufficiente per creare l'hive del registro di sistema, la funzione restituisce un errore di \_ \_ memoria insufficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="86dbb-114">If there is insufficient memory to create the registry hive, the function returns ERROR\_NOT\_ENOUGH\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="86dbb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="86dbb-115">Remarks</span></span>

<span data-ttu-id="86dbb-116">La funzione **ORCreateHive** crea un hive del registro di sistema offline vuoto in memoria.</span><span class="sxs-lookup"><span data-stu-id="86dbb-116">The **ORCreateHive** function creates an empty offline registry hive in memory.</span></span> <span data-ttu-id="86dbb-117">Usare le funzioni [**ORCreateKey**](orcreatekey.md) e [**ORSetValue**](orsetvalue.md) per aggiungere chiavi e impostare i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="86dbb-117">Use the [**ORCreateKey**](orcreatekey.md) and [**ORSetValue**](orsetvalue.md) functions to add keys and set their values.</span></span>

## <a name="requirements"></a><span data-ttu-id="86dbb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86dbb-118">Requirements</span></span>



| <span data-ttu-id="86dbb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86dbb-119">Requirement</span></span> | <span data-ttu-id="86dbb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="86dbb-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86dbb-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="86dbb-121">Redistributable</span></span><br/> | <span data-ttu-id="86dbb-122">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="86dbb-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="86dbb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86dbb-123">Header</span></span><br/>          | <dl> <span data-ttu-id="86dbb-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="86dbb-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="86dbb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="86dbb-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="86dbb-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86dbb-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86dbb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86dbb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86dbb-128">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="86dbb-128">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="86dbb-129">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="86dbb-129">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="86dbb-130">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="86dbb-130">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="86dbb-131">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="86dbb-131">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
