---
description: Ottiene le proprietà della visualizzazione.
title: 'Metodo IShellFolderViewType:: GetViewTypeProperties'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977927"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="4a2b1-103">Metodo IShellFolderViewType:: GetViewTypeProperties</span><span class="sxs-lookup"><span data-stu-id="4a2b1-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="4a2b1-104">Ottiene le proprietà della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a2b1-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4a2b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a2b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a2b1-107">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-108">Tipo: **PCUITEMID \_ figlio**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="4a2b1-109">PIDL.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="4a2b1-110">*pdwFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="4a2b1-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="4a2b1-112">Puntatore a una variabile Unsigned Integer che riceve le proprietà di visualizzazione, che indicano l'azione da eseguire quando la visualizzazione è selezionata.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="4a2b1-113">I flag possono essere costituiti da qualsiasi combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="4a2b1-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG \_ Notify \_ create*\* (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4a2b1-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG\_NOTIFY\_CREATE*\* (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="4a2b1-115">Crea elemento visualizzazione se non è presente.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="4a2b1-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ Resort** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="4a2b1-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="4a2b1-117">Reinserire PIDL ed eseguire di nuovo l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a2b1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a2b1-118">Return value</span></span>

<span data-ttu-id="4a2b1-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-119">Type: **HRESULT**</span></span>

<span data-ttu-id="4a2b1-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a2b1-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a2b1-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2b1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a2b1-122">Requirements</span></span>



| <span data-ttu-id="4a2b1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2b1-123">Requirement</span></span> | <span data-ttu-id="4a2b1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4a2b1-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2b1-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a2b1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2b1-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4a2b1-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a2b1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2b1-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a2b1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4a2b1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a2b1-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a2b1-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




