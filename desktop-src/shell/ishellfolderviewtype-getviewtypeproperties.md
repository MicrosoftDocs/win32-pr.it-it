---
description: Ottiene le proprietà della visualizzazione.
title: Metodo IShellFolderViewType::GetViewTypeProperties
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
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842702"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="8ed17-103">Metodo IShellFolderViewType::GetViewTypeProperties</span><span class="sxs-lookup"><span data-stu-id="8ed17-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="8ed17-104">Ottiene le proprietà della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8ed17-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed17-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ed17-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8ed17-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ed17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed17-107">*pidl* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8ed17-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed17-108">Tipo: **PCUITEMID \_ CHILD**</span><span class="sxs-lookup"><span data-stu-id="8ed17-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="8ed17-109">Oggetto PIDL.</span><span class="sxs-lookup"><span data-stu-id="8ed17-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="8ed17-110">*pdwFlags* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="8ed17-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed17-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="8ed17-111">Type: **DWORD\***</span></span>

<span data-ttu-id="8ed17-112">Puntatore a una variabile unsigned integer che riceve le proprietà della visualizzazione, che indicano l'operazione da eseguire quando viene selezionata la vista.</span><span class="sxs-lookup"><span data-stu-id="8ed17-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="8ed17-113">I flag possono essere qualsiasi combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ed17-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="8ed17-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFY \_ CREATE** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="8ed17-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG\_NOTIFY\_CREATE** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="8ed17-115">Se non è presente, creare un elemento di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8ed17-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="8ed17-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ RESORT** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="8ed17-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="8ed17-117">Reinserisci PIDL e riordina.</span><span class="sxs-lookup"><span data-stu-id="8ed17-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ed17-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ed17-118">Return value</span></span>

<span data-ttu-id="8ed17-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8ed17-119">Type: **HRESULT**</span></span>

<span data-ttu-id="8ed17-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8ed17-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ed17-121">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="8ed17-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed17-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ed17-122">Requirements</span></span>



| <span data-ttu-id="8ed17-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed17-123">Requirement</span></span> | <span data-ttu-id="8ed17-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8ed17-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed17-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ed17-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed17-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8ed17-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8ed17-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ed17-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed17-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8ed17-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8ed17-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8ed17-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ed17-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ed17-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




