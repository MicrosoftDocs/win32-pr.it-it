---
description: Crea un nuovo database shim.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966116"
---
# <a name="sdbcreatedatabase-function"></a><span data-ttu-id="5cee9-103">SdbCreateDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="5cee9-103">SdbCreateDatabase function</span></span>

<span data-ttu-id="5cee9-104">Crea un nuovo database shim.</span><span class="sxs-lookup"><span data-stu-id="5cee9-104">Creates a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cee9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cee9-105">Syntax</span></span>


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="5cee9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cee9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cee9-107">*pwszPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cee9-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cee9-108">Percorso in cui salvare il database.</span><span class="sxs-lookup"><span data-stu-id="5cee9-108">The path where the database should be saved.</span></span> <span data-ttu-id="5cee9-109">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5cee9-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5cee9-110">*etype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cee9-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cee9-111">Tipo di percorso.</span><span class="sxs-lookup"><span data-stu-id="5cee9-111">The path type.</span></span> <span data-ttu-id="5cee9-112">Per un elenco di valori, vedere [**\_ tipo di percorso**](path-type.md) .</span><span class="sxs-lookup"><span data-stu-id="5cee9-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cee9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cee9-113">Return value</span></span>

<span data-ttu-id="5cee9-114">La funzione restituisce un handle per il database shim o **null** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="5cee9-114">The function returns a handle to the shim database or **NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cee9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cee9-115">Requirements</span></span>



| <span data-ttu-id="5cee9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cee9-116">Requirement</span></span> | <span data-ttu-id="5cee9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5cee9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cee9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cee9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5cee9-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cee9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5cee9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cee9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5cee9-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5cee9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5cee9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5cee9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cee9-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cee9-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cee9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cee9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cee9-125">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="5cee9-125">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




