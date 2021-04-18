---
description: Recupera l'indice per il tag e il tipo di chiave specificati dal database specificato.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483229"
---
# <a name="sdbgetindex-function"></a><span data-ttu-id="35e89-103">SdbGetIndex (funzione)</span><span class="sxs-lookup"><span data-stu-id="35e89-103">SdbGetIndex function</span></span>

<span data-ttu-id="35e89-104">Recupera l'indice per il tag e il tipo di chiave specificati dal database specificato.</span><span class="sxs-lookup"><span data-stu-id="35e89-104">Retrieves the index for the specified tag and key type from the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e89-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35e89-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="35e89-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35e89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e89-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e89-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e89-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="35e89-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="35e89-109">*tWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e89-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e89-110">TAG.</span><span class="sxs-lookup"><span data-stu-id="35e89-110">The TAG.</span></span>

</dd> <dt>

<span data-ttu-id="35e89-111">*tKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e89-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e89-112">Tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="35e89-112">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="35e89-113">*lpdwFlags* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35e89-113">*lpdwFlags* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35e89-114">Questo parametro può essere 0 o **la \_ \_ \_ chiave univoca dell'indice SHIMDB** (0x00000001).</span><span class="sxs-lookup"><span data-stu-id="35e89-114">This parameter can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e89-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35e89-115">Return value</span></span>

<span data-ttu-id="35e89-116">**TagId** dell'indice o **TagId \_ null**.</span><span class="sxs-lookup"><span data-stu-id="35e89-116">The **TAGID** of the index or **TAGID\_NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e89-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="35e89-117">Remarks</span></span>

<span data-ttu-id="35e89-118">L'indice risultante può essere utilizzato per le operazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="35e89-118">The resulting index can be used for read operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e89-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35e89-119">Requirements</span></span>



| <span data-ttu-id="35e89-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e89-120">Requirement</span></span> | <span data-ttu-id="35e89-121">Valore</span><span class="sxs-lookup"><span data-stu-id="35e89-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35e89-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35e89-122">Minimum supported client</span></span><br/> | <span data-ttu-id="35e89-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35e89-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="35e89-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35e89-124">Minimum supported server</span></span><br/> | <span data-ttu-id="35e89-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35e89-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35e89-126">DLL</span><span class="sxs-lookup"><span data-stu-id="35e89-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e89-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35e89-127"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




