---
description: Rende questo puntatore a un elenco di identificatori di elemento (PIDL) una parte non valida della cartella shell.
title: Metodo IShellFolderSearchable::InvalidateSearch
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
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841692"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="65aa7-103">Metodo IShellFolderSearchable::InvalidateSearch</span><span class="sxs-lookup"><span data-stu-id="65aa7-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="65aa7-104">Rende questo puntatore a un elenco di identificatori di elemento (PIDL) una parte non valida della cartella shell.</span><span class="sxs-lookup"><span data-stu-id="65aa7-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="65aa7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65aa7-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="65aa7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65aa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65aa7-107">*pidlSearch* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65aa7-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65aa7-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="65aa7-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="65aa7-109">Puntatore alla [**struttura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la cartella di ricerca.</span><span class="sxs-lookup"><span data-stu-id="65aa7-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="65aa7-110">*pdwFlags* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65aa7-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65aa7-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="65aa7-111">Type: **DWORD\***</span></span>

<span data-ttu-id="65aa7-112">Nessun flag è attualmente definito. impostato su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="65aa7-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65aa7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65aa7-113">Return value</span></span>

<span data-ttu-id="65aa7-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="65aa7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="65aa7-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="65aa7-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65aa7-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="65aa7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65aa7-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="65aa7-117">Remarks</span></span>

<span data-ttu-id="65aa7-118">Quando una cartella di ricerca viene invalidata, può eseguire la pulizia di tutte le risorse usate.</span><span class="sxs-lookup"><span data-stu-id="65aa7-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="65aa7-119">Il **metodo IShellFolderSearchable::InvalidateSearch** può causare l'annullamento di una ricerca asincrona e comporterà la versione finale dell'oggetto [**interfaccia IShellFolderSearchableCallback.**](ishellfoldersearchablecallback.md)</span><span class="sxs-lookup"><span data-stu-id="65aa7-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="65aa7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65aa7-120">Requirements</span></span>



| <span data-ttu-id="65aa7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="65aa7-121">Requirement</span></span> | <span data-ttu-id="65aa7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="65aa7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65aa7-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65aa7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="65aa7-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65aa7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="65aa7-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65aa7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="65aa7-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65aa7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="65aa7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="65aa7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65aa7-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65aa7-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




