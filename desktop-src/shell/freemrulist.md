---
description: Libera l'handle associato all'elenco degli ultimi elementi usati (MRU) e scrive i dati memorizzati nella cache nel registro di sistema.
title: FreeMRUList (funzione)
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
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979650"
---
# <a name="freemrulist-function"></a><span data-ttu-id="97d77-103">FreeMRUList (funzione)</span><span class="sxs-lookup"><span data-stu-id="97d77-103">FreeMRUList function</span></span>

<span data-ttu-id="97d77-104">Libera l'handle associato all'elenco degli ultimi elementi usati (MRU) e scrive i dati memorizzati nella cache nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="97d77-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d77-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97d77-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="97d77-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97d77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d77-107">*hMRU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97d77-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d77-108">Tipo: **handle**</span><span class="sxs-lookup"><span data-stu-id="97d77-108">Type: **HANDLE**</span></span>

<span data-ttu-id="97d77-109">Handle dell'elenco MRU da liberare.</span><span class="sxs-lookup"><span data-stu-id="97d77-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d77-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97d77-110">Return value</span></span>

<span data-ttu-id="97d77-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="97d77-111">Type: **int**</span></span>

<span data-ttu-id="97d77-112">Restituisce un valore non negativo se ha esito positivo,-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="97d77-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="97d77-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="97d77-113">Remarks</span></span>

<span data-ttu-id="97d77-114">Se l'elenco MRU è stato creato con il flag **\_ CACHEWRITE di MRU** , la chiamata a **FreeMRUList** comporta la scrittura in questo momento di eventuali modifiche non ancora scritte nella versione dell'elenco MRU archiviato nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="97d77-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="97d77-115">Questa funzione non è inclusa in un'intestazione o in una libreria pubblica.</span><span class="sxs-lookup"><span data-stu-id="97d77-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="97d77-116">Deve essere estratta da comctl32.dll in base all'ordinale 152.</span><span class="sxs-lookup"><span data-stu-id="97d77-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d77-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97d77-117">Requirements</span></span>



| <span data-ttu-id="97d77-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="97d77-118">Requirement</span></span> | <span data-ttu-id="97d77-119">Valore</span><span class="sxs-lookup"><span data-stu-id="97d77-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97d77-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97d77-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97d77-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97d77-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97d77-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97d77-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97d77-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97d77-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="97d77-124">DLL</span><span class="sxs-lookup"><span data-stu-id="97d77-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97d77-125"><dt>Comctl32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="97d77-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




