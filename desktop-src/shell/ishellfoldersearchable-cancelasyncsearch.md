---
description: Avvia il processo di annullamento di una ricerca asincrona in sospeso.
title: Metodo IShellFolderSearchable::CancelAsyncSearch
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
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842992"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="04d36-103">Metodo IShellFolderSearchable::CancelAsyncSearch</span><span class="sxs-lookup"><span data-stu-id="04d36-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="04d36-104">Avvia il processo di annullamento di una ricerca asincrona in sospeso.</span><span class="sxs-lookup"><span data-stu-id="04d36-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d36-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04d36-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="04d36-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04d36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d36-107">*pidlSearch* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="04d36-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04d36-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="04d36-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="04d36-109">Puntatore a un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="04d36-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="04d36-110">*pdwFlags* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="04d36-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04d36-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="04d36-111">Type: **DWORD\***</span></span>

<span data-ttu-id="04d36-112">Non è attualmente definito alcun flag. impostato su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="04d36-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d36-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04d36-113">Return value</span></span>

<span data-ttu-id="04d36-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="04d36-114">Type: **HRESULT**</span></span>

<span data-ttu-id="04d36-115">Restituisce S \_ OK in caso di annullamento oppure S FALSE se la ricerca non è in \_ esecuzione.</span><span class="sxs-lookup"><span data-stu-id="04d36-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d36-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="04d36-116">Remarks</span></span>

<span data-ttu-id="04d36-117">Quando la ricerca viene effettivamente annullata, [**viene chiamato RunEnd.**](ishellfoldersearchablecallback-runend.md)</span><span class="sxs-lookup"><span data-stu-id="04d36-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d36-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04d36-118">Requirements</span></span>



| <span data-ttu-id="04d36-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04d36-119">Requirement</span></span> | <span data-ttu-id="04d36-120">Valore</span><span class="sxs-lookup"><span data-stu-id="04d36-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04d36-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04d36-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04d36-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04d36-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="04d36-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04d36-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04d36-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04d36-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04d36-125">DLL</span><span class="sxs-lookup"><span data-stu-id="04d36-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04d36-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d36-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




