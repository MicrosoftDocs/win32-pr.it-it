---
description: Chiude il database shim inizializzato utilizzando la funzione SdbInitDatabase.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: SdbReleaseDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523337"
---
# <a name="sdbreleasedatabase-function"></a><span data-ttu-id="e5a6e-103">SdbReleaseDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="e5a6e-103">SdbReleaseDatabase function</span></span>

<span data-ttu-id="e5a6e-104">Chiude il database shim inizializzato utilizzando la funzione [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a6e-104">Closes the shim database initialized using the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5a6e-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a><span data-ttu-id="e5a6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5a6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a6e-107">*hSDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5a6e-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a6e-108">Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a6e-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a6e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5a6e-109">Return value</span></span>

<span data-ttu-id="e5a6e-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e5a6e-110">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a6e-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5a6e-111">Requirements</span></span>



| <span data-ttu-id="e5a6e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5a6e-112">Requirement</span></span> | <span data-ttu-id="e5a6e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e5a6e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a6e-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5a6e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a6e-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5a6e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e5a6e-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5a6e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a6e-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5a6e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e5a6e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a6e-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a6e-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a6e-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a6e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5a6e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a6e-121">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="e5a6e-121">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




