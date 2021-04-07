---
description: Apre il database shim specificato.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747855"
---
# <a name="sdbopendatabase-function"></a><span data-ttu-id="d7631-103">SdbOpenDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="d7631-103">SdbOpenDatabase function</span></span>

<span data-ttu-id="d7631-104">Apre il database shim specificato.</span><span class="sxs-lookup"><span data-stu-id="d7631-104">Opens the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7631-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7631-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="d7631-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7631-107">*pwszPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7631-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7631-108">Percorso del database.</span><span class="sxs-lookup"><span data-stu-id="d7631-108">The database path.</span></span> <span data-ttu-id="d7631-109">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d7631-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d7631-110">*etype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7631-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7631-111">Tipo di percorso.</span><span class="sxs-lookup"><span data-stu-id="d7631-111">The path type.</span></span> <span data-ttu-id="d7631-112">Per un elenco di valori, vedere [**\_ tipo di percorso**](path-type.md) .</span><span class="sxs-lookup"><span data-stu-id="d7631-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7631-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7631-113">Return value</span></span>

<span data-ttu-id="d7631-114">La funzione restituisce un handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="d7631-114">The function returns a handle to the shim database.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7631-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7631-115">Requirements</span></span>



| <span data-ttu-id="d7631-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7631-116">Requirement</span></span> | <span data-ttu-id="d7631-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d7631-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7631-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7631-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d7631-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d7631-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d7631-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7631-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d7631-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7631-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d7631-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d7631-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7631-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7631-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7631-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7631-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7631-125">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="d7631-125">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> </dl>

 

 




