---
description: Recupera i dati di stringa per il TAGID specificato.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: SdbGetStringTagPtr (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966115"
---
# <a name="sdbgetstringtagptr-function"></a><span data-ttu-id="500d8-103">SdbGetStringTagPtr (funzione)</span><span class="sxs-lookup"><span data-stu-id="500d8-103">SdbGetStringTagPtr function</span></span>

<span data-ttu-id="500d8-104">Recupera i dati di stringa per il **TagId** specificato.</span><span class="sxs-lookup"><span data-stu-id="500d8-104">Retrieves the string data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="500d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="500d8-105">Syntax</span></span>


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="500d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="500d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="500d8-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="500d8-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="500d8-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="500d8-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="500d8-109">*tiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="500d8-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="500d8-110">**TagId** che corrisponde ai dati stringa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="500d8-110">The **TAGID** that corresponds to the string data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="500d8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="500d8-111">Return value</span></span>

<span data-ttu-id="500d8-112">La funzione restituisce un puntatore ai dati di tipo stringa o **null** se **TagId** non è valido o non è di tipo **\_ \_ stringa** o **tipo di tag \_ \_ STRINGREF**.</span><span class="sxs-lookup"><span data-stu-id="500d8-112">The function returns a pointer to the string data or **NULL** if the **TAGID** is invalid or not of type **TAG\_TYPE\_STRING** or **TAG\_TYPE\_STRINGREF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="500d8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="500d8-113">Requirements</span></span>



| <span data-ttu-id="500d8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="500d8-114">Requirement</span></span> | <span data-ttu-id="500d8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="500d8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="500d8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="500d8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="500d8-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="500d8-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="500d8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="500d8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="500d8-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="500d8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="500d8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="500d8-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="500d8-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="500d8-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="500d8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="500d8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="500d8-123">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="500d8-123">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="500d8-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="500d8-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="500d8-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="500d8-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="500d8-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="500d8-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




