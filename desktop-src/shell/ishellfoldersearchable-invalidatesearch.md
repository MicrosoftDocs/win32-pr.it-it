---
description: Rende questo puntatore a un elenco di identificatori di elemento (PIDL) una parte non valida della cartella della shell.
title: 'Metodo IShellFolderSearchable:: InvalidateSearch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226364"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="d426a-103">Metodo IShellFolderSearchable:: InvalidateSearch</span><span class="sxs-lookup"><span data-stu-id="d426a-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="d426a-104">Rende questo puntatore a un elenco di identificatori di elemento (PIDL) una parte non valida della cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="d426a-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="d426a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d426a-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d426a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d426a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d426a-107">*pidlSearch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d426a-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d426a-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="d426a-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="d426a-109">Puntatore alla struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la cartella di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d426a-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="d426a-110">*pdwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d426a-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d426a-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="d426a-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="d426a-112">Nessun flag attualmente definito. impostare su _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="d426a-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d426a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d426a-113">Return value</span></span>

<span data-ttu-id="d426a-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d426a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d426a-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d426a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d426a-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d426a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d426a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d426a-117">Remarks</span></span>

<span data-ttu-id="d426a-118">Quando una cartella di ricerca viene invalidata, può eseguire la pulizia delle risorse usate.</span><span class="sxs-lookup"><span data-stu-id="d426a-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="d426a-119">Il metodo **IShellFolderSearchable:: InvalidateSearch** può causare l'annullamento di una ricerca asincrona e comporterà la versione finale dell'oggetto interfaccia [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="d426a-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d426a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d426a-120">Requirements</span></span>



| <span data-ttu-id="d426a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d426a-121">Requirement</span></span> | <span data-ttu-id="d426a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d426a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d426a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d426a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d426a-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d426a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d426a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d426a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d426a-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d426a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d426a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d426a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d426a-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d426a-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




