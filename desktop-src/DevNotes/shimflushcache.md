---
description: Svuota la cache del database shim. Questa funzione deve essere chiamata dopo l'installazione di un nuovo database shim.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049078"
---
# <a name="shimflushcache-function"></a><span data-ttu-id="7638a-104">ShimFlushCache (funzione)</span><span class="sxs-lookup"><span data-stu-id="7638a-104">ShimFlushCache function</span></span>

<span data-ttu-id="7638a-105">Svuota la cache del database shim.</span><span class="sxs-lookup"><span data-stu-id="7638a-105">Flushes the shim database cache.</span></span> <span data-ttu-id="7638a-106">Questa funzione deve essere chiamata dopo l'installazione di un nuovo database shim.</span><span class="sxs-lookup"><span data-stu-id="7638a-106">This function should be called after installing a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7638a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7638a-107">Syntax</span></span>


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="7638a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7638a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7638a-109">*HWND* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7638a-109">*hwnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7638a-110">Inutilizzati deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="7638a-110">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="7638a-111">*HINSTANCE* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7638a-111">*hInstance* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7638a-112">Inutilizzati deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="7638a-112">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="7638a-113">*lpszCmdLine* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7638a-113">*lpszCmdLine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7638a-114">Inutilizzati deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="7638a-114">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="7638a-115">*nCmdShow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7638a-115">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7638a-116">Inutilizzati deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="7638a-116">Unused; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7638a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7638a-117">Return value</span></span>

<span data-ttu-id="7638a-118">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="7638a-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7638a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7638a-119">Remarks</span></span>

<span data-ttu-id="7638a-120">Il chiamante deve essere un amministratore.</span><span class="sxs-lookup"><span data-stu-id="7638a-120">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="7638a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7638a-121">Requirements</span></span>



| <span data-ttu-id="7638a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7638a-122">Requirement</span></span> | <span data-ttu-id="7638a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7638a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7638a-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7638a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7638a-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7638a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7638a-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7638a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7638a-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7638a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7638a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7638a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7638a-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7638a-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7638a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7638a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7638a-131">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="7638a-131">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
</dt> </dl>

 

 




