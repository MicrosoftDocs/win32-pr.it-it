---
description: Recupera TAGID e un handle per il database shim per il TAGREF specificato.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: SdbTagRefToTagID (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126387"
---
# <a name="sdbtagreftotagid-function"></a><span data-ttu-id="bf7c5-103">SdbTagRefToTagID (funzione)</span><span class="sxs-lookup"><span data-stu-id="bf7c5-103">SdbTagRefToTagID function</span></span>

<span data-ttu-id="bf7c5-104">Recupera **TagId** e un handle per il database shim per il [**TAGREF**](tagref.md)specificato.</span><span class="sxs-lookup"><span data-stu-id="bf7c5-104">Retrieves the **TAGID** and a handle to the shim database for the specified [**TAGREF**](tagref.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf7c5-105">Syntax</span></span>


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="bf7c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf7c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf7c5-107">*hSDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf7c5-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7c5-108">Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="bf7c5-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bf7c5-109">*trWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf7c5-109">*trWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7c5-110">[**TAGREF**](tagref.md).</span><span class="sxs-lookup"><span data-stu-id="bf7c5-110">The [**TAGREF**](tagref.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf7c5-111">*PPDB* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bf7c5-111">*ppdb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7c5-112">Handle risultante per il database shim.</span><span class="sxs-lookup"><span data-stu-id="bf7c5-112">The resulting handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="bf7c5-113">*ptiWhich* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bf7c5-113">*ptiWhich* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7c5-114">**TagId** risultante.</span><span class="sxs-lookup"><span data-stu-id="bf7c5-114">The resulting **TAGID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf7c5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf7c5-115">Return value</span></span>

<span data-ttu-id="bf7c5-116">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="bf7c5-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7c5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf7c5-117">Requirements</span></span>



| <span data-ttu-id="bf7c5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf7c5-118">Requirement</span></span> | <span data-ttu-id="bf7c5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bf7c5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7c5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf7c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7c5-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bf7c5-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bf7c5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf7c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7c5-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf7c5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bf7c5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bf7c5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf7c5-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf7c5-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf7c5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf7c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7c5-127">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="bf7c5-127">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="bf7c5-128">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="bf7c5-128">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="bf7c5-129">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="bf7c5-129">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




