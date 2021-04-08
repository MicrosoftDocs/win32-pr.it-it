---
description: Chiude il database specificato.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: SdbCloseDatabaseWrite (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877629"
---
# <a name="sdbclosedatabasewrite-function"></a><span data-ttu-id="1c97c-103">SdbCloseDatabaseWrite (funzione)</span><span class="sxs-lookup"><span data-stu-id="1c97c-103">SdbCloseDatabaseWrite function</span></span>

<span data-ttu-id="1c97c-104">Chiude il database specificato.</span><span class="sxs-lookup"><span data-stu-id="1c97c-104">Closes the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c97c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c97c-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="1c97c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c97c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c97c-107">*PDB* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1c97c-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c97c-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="1c97c-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c97c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c97c-109">Return value</span></span>

<span data-ttu-id="1c97c-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1c97c-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c97c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c97c-111">Remarks</span></span>

<span data-ttu-id="1c97c-112">Questa funzione chiama [**SdbCloseDatabase**](sdbclosedatabase.md); Queste due funzioni sono pertanto equivalenti.</span><span class="sxs-lookup"><span data-stu-id="1c97c-112">This function calls [**SdbCloseDatabase**](sdbclosedatabase.md); therefore, these two functions are equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c97c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c97c-113">Requirements</span></span>



| <span data-ttu-id="1c97c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c97c-114">Requirement</span></span> | <span data-ttu-id="1c97c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1c97c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c97c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c97c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c97c-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c97c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1c97c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c97c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c97c-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c97c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1c97c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1c97c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c97c-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c97c-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c97c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c97c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c97c-123">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="1c97c-123">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="1c97c-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="1c97c-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="1c97c-125">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="1c97c-125">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> </dl>

 

 




