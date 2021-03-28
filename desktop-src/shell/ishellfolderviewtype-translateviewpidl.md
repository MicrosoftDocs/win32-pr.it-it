---
description: Ricostruisce un puntatore a un elenco di identificatori di elemento (PIDL) da una rappresentazione gerarchica della cartella della shell in una rappresentazione diversa.
title: 'Metodo IShellFolderViewType:: TranslateViewPidl'
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
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527312"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="46b8e-103">Metodo IShellFolderViewType:: TranslateViewPidl</span><span class="sxs-lookup"><span data-stu-id="46b8e-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="46b8e-104">Ricostruisce un puntatore a un elenco di identificatori di elemento (PIDL) da una rappresentazione gerarchica della cartella della shell in una rappresentazione diversa.</span><span class="sxs-lookup"><span data-stu-id="46b8e-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="46b8e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46b8e-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="46b8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46b8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46b8e-107">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46b8e-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8e-108">Tipo: **PCUIDLIST \_ relativo**</span><span class="sxs-lookup"><span data-stu-id="46b8e-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="46b8e-109">Matrice di ID elemento rispetto alla cartella radice.</span><span class="sxs-lookup"><span data-stu-id="46b8e-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="46b8e-110">*pidlView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46b8e-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8e-111">Tipo: **PCUIDLIST \_ relativo**</span><span class="sxs-lookup"><span data-stu-id="46b8e-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="46b8e-112">PIDL speciale della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="46b8e-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="46b8e-113">*ppidlOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46b8e-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46b8e-114">Tipo: \**PCUIDLIST \_ relativo \** _</span><span class="sxs-lookup"><span data-stu-id="46b8e-114">Type: \**PCUIDLIST\_RELATIVE\** _</span></span>

<span data-ttu-id="46b8e-115">Indirizzo di una variabile PIDL per ricevere la traduzione.</span><span class="sxs-lookup"><span data-stu-id="46b8e-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46b8e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46b8e-116">Return value</span></span>

<span data-ttu-id="46b8e-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="46b8e-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="46b8e-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46b8e-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46b8e-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46b8e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46b8e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="46b8e-120">Remarks</span></span>

<span data-ttu-id="46b8e-121">Al termine, è necessario liberare il PIDL restituito con [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span><span class="sxs-lookup"><span data-stu-id="46b8e-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="46b8e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46b8e-122">Requirements</span></span>



| <span data-ttu-id="46b8e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b8e-123">Requirement</span></span> | <span data-ttu-id="46b8e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="46b8e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46b8e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b8e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="46b8e-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46b8e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="46b8e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b8e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="46b8e-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46b8e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="46b8e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="46b8e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46b8e-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46b8e-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




