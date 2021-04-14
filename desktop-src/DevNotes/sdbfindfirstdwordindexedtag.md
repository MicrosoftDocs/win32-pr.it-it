---
description: Trova il primo record DWORD nell'indice specificato che soddisfa i criteri specificati.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522817"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a><span data-ttu-id="27366-103">SdbFindFirstDWORDIndexedTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="27366-103">SdbFindFirstDWORDIndexedTag function</span></span>

<span data-ttu-id="27366-104">Trova il primo record **DWORD** nell'indice specificato che soddisfa i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="27366-104">Finds the first **DWORD** record in the specified index that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="27366-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27366-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a><span data-ttu-id="27366-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27366-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27366-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27366-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27366-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="27366-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="27366-109">*tWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27366-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27366-110">Tipo di indice.</span><span class="sxs-lookup"><span data-stu-id="27366-110">The index type.</span></span> <span data-ttu-id="27366-111">Per un elenco di valori, vedere [**tag**](tag.md) .</span><span class="sxs-lookup"><span data-stu-id="27366-111">See [**TAG**](tag.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="27366-112">*tKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27366-112">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27366-113">Tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="27366-113">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="27366-114">*dwName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27366-114">*dwName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27366-115">Nome dei dati da trovare.</span><span class="sxs-lookup"><span data-stu-id="27366-115">The name of the data to be found.</span></span> <span data-ttu-id="27366-116">Questo valore verrà convertito in una chiave.</span><span class="sxs-lookup"><span data-stu-id="27366-116">This value will be converted into a key.</span></span>

</dd> <dt>

<span data-ttu-id="27366-117">*pFindInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27366-117">*pFindInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27366-118">Struttura [**di \_ informazioni di ricerca**](find-info.md) che riceve il record.</span><span class="sxs-lookup"><span data-stu-id="27366-118">A [**FIND\_INFO**](find-info.md) structure that receives the record.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27366-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27366-119">Return value</span></span>

<span data-ttu-id="27366-120">**TagId** della prima corrispondenza o **tag \_ null** se non viene trovata alcuna corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="27366-120">The **TAGID** of the first match or **TAG\_NULL** if no match is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="27366-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27366-121">Requirements</span></span>



| <span data-ttu-id="27366-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="27366-122">Requirement</span></span> | <span data-ttu-id="27366-123">Valore</span><span class="sxs-lookup"><span data-stu-id="27366-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27366-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27366-124">Minimum supported client</span></span><br/> | <span data-ttu-id="27366-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27366-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="27366-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27366-126">Minimum supported server</span></span><br/> | <span data-ttu-id="27366-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27366-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="27366-128">DLL</span><span class="sxs-lookup"><span data-stu-id="27366-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27366-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27366-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27366-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27366-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27366-131">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="27366-131">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> </dl>

 

 




