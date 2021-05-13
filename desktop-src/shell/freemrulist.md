---
description: Libera l'handle associato all'elenco MRU (Most Recently Used) e scrive i dati memorizzati nella cache nel Registro di sistema.
title: Funzione FreeMRUList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840622"
---
# <a name="freemrulist-function"></a><span data-ttu-id="0a582-103">Funzione FreeMRUList</span><span class="sxs-lookup"><span data-stu-id="0a582-103">FreeMRUList function</span></span>

<span data-ttu-id="0a582-104">Libera l'handle associato all'elenco MRU (Most Recently Used) e scrive i dati memorizzati nella cache nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0a582-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a582-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a582-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="0a582-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a582-107">*hMRU* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0a582-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a582-108">Tipo: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="0a582-108">Type: **HANDLE**</span></span>

<span data-ttu-id="0a582-109">Handle dell'elenco MRU da liberare.</span><span class="sxs-lookup"><span data-stu-id="0a582-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a582-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a582-110">Return value</span></span>

<span data-ttu-id="0a582-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0a582-111">Type: **int**</span></span>

<span data-ttu-id="0a582-112">Restituisce un valore non negativo in caso di esito positivo, -1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0a582-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a582-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a582-113">Remarks</span></span>

<span data-ttu-id="0a582-114">Se l'elenco MRU è stato creato usando il flag **MRU \_ CACHEWRITE,** la chiamata a **FreeMRUList** determina la scrittura di tutte le modifiche non ancora scritte nella versione dell'elenco MRU archiviata nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0a582-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="0a582-115">Questa funzione non è inclusa in un'intestazione o in una libreria pubblica.</span><span class="sxs-lookup"><span data-stu-id="0a582-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="0a582-116">Deve essere estratto da comctl32.dll ordinale 152.</span><span class="sxs-lookup"><span data-stu-id="0a582-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a582-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a582-117">Requirements</span></span>



| <span data-ttu-id="0a582-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a582-118">Requirement</span></span> | <span data-ttu-id="0a582-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0a582-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a582-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a582-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0a582-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a582-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a582-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a582-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0a582-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a582-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0a582-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0a582-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a582-125"><dt>Comctl32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0a582-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




