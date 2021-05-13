---
description: Ricostruisce un puntatore a un elenco di identificatori di elemento (PIDL) da una rappresentazione gerarchica della cartella Shell in una rappresentazione diversa.
title: Metodo IShellFolderViewType::TranslateViewPidl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 537a77e7ffffb462e0031ea0959f60cd695f7d99
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842672"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="69440-103">Metodo IShellFolderViewType::TranslateViewPidl</span><span class="sxs-lookup"><span data-stu-id="69440-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="69440-104">Ricostruisce un puntatore a un elenco di identificatori di elemento (PIDL) da una rappresentazione gerarchica della cartella Shell in una rappresentazione diversa.</span><span class="sxs-lookup"><span data-stu-id="69440-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="69440-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69440-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="69440-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69440-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69440-107">*pidl* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="69440-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69440-108">Tipo: **PCUIDLIST \_ RELATIVE**</span><span class="sxs-lookup"><span data-stu-id="69440-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="69440-109">Matrice di ID elemento relativi alla cartella radice.</span><span class="sxs-lookup"><span data-stu-id="69440-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="69440-110">*pidlView* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="69440-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69440-111">Tipo: **PCUIDLIST \_ RELATIVE**</span><span class="sxs-lookup"><span data-stu-id="69440-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="69440-112">PIDL speciale della vista.</span><span class="sxs-lookup"><span data-stu-id="69440-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="69440-113">*ppidlOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="69440-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69440-114">Tipo: **PCUIDLIST \_ RELATIVE \***</span><span class="sxs-lookup"><span data-stu-id="69440-114">Type: **PCUIDLIST\_RELATIVE\***</span></span>

<span data-ttu-id="69440-115">Indirizzo di una variabile PIDL per ricevere la traduzione.</span><span class="sxs-lookup"><span data-stu-id="69440-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69440-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69440-116">Return value</span></span>

<span data-ttu-id="69440-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="69440-117">Type: **HRESULT**</span></span>

<span data-ttu-id="69440-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="69440-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69440-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="69440-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="69440-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="69440-120">Remarks</span></span>

<span data-ttu-id="69440-121">Al termine, è necessario liberare il FILE PIDL restituito con [**ILFree.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree)</span><span class="sxs-lookup"><span data-stu-id="69440-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="69440-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69440-122">Requirements</span></span>



| <span data-ttu-id="69440-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="69440-123">Requirement</span></span> | <span data-ttu-id="69440-124">Valore</span><span class="sxs-lookup"><span data-stu-id="69440-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69440-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69440-125">Minimum supported client</span></span><br/> | <span data-ttu-id="69440-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69440-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="69440-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69440-127">Minimum supported server</span></span><br/> | <span data-ttu-id="69440-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69440-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69440-129">DLL</span><span class="sxs-lookup"><span data-stu-id="69440-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69440-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69440-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




