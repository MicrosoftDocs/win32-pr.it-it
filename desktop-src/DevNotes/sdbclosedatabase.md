---
description: Chiude il database shim specificato.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: SdbCloseDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049177"
---
# <a name="sdbclosedatabase-function"></a><span data-ttu-id="8b589-103">SdbCloseDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="8b589-103">SdbCloseDatabase function</span></span>

<span data-ttu-id="8b589-104">Chiude il database shim specificato.</span><span class="sxs-lookup"><span data-stu-id="8b589-104">Closes the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b589-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b589-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="8b589-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b589-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b589-107">*PDB* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8b589-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b589-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="8b589-108">A handle to the shim database.</span></span> <span data-ttu-id="8b589-109">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8b589-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b589-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b589-110">Return value</span></span>

<span data-ttu-id="8b589-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8b589-111">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b589-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b589-112">Requirements</span></span>



| <span data-ttu-id="8b589-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b589-113">Requirement</span></span> | <span data-ttu-id="8b589-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8b589-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b589-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b589-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8b589-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b589-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b589-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b589-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8b589-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b589-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8b589-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8b589-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b589-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b589-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b589-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b589-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b589-122">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="8b589-122">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




