---
description: Inizia il processo di annullamento di una ricerca asincrona in sospeso.
title: 'Metodo IShellFolderSearchable:: CancelAsyncSearch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977954"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="8883e-103">Metodo IShellFolderSearchable:: CancelAsyncSearch</span><span class="sxs-lookup"><span data-stu-id="8883e-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="8883e-104">Inizia il processo di annullamento di una ricerca asincrona in sospeso.</span><span class="sxs-lookup"><span data-stu-id="8883e-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="8883e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8883e-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8883e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8883e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8883e-107">*pidlSearch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8883e-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8883e-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="8883e-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="8883e-109">Puntatore a un oggetto [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="8883e-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="8883e-110">*pdwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8883e-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8883e-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="8883e-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="8883e-112">Nessun flag attualmente definito. impostare su _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="8883e-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8883e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8883e-113">Return value</span></span>

<span data-ttu-id="8883e-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8883e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8883e-115">Restituisce \_ OK se viene annullata o \_ è false se la ricerca non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8883e-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="8883e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8883e-116">Remarks</span></span>

<span data-ttu-id="8883e-117">Quando la ricerca viene effettivamente annullata, verrà chiamato [**RunEnd**](ishellfoldersearchablecallback-runend.md) .</span><span class="sxs-lookup"><span data-stu-id="8883e-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8883e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8883e-118">Requirements</span></span>



| <span data-ttu-id="8883e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8883e-119">Requirement</span></span> | <span data-ttu-id="8883e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8883e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8883e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8883e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8883e-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8883e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8883e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8883e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8883e-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8883e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8883e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8883e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8883e-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8883e-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




