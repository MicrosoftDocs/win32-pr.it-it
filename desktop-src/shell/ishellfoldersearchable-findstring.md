---
description: Inizia una ricerca di una stringa di ricerca specificata.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'Metodo IShellFolderSearchable:: FindString (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753063"
---
# <a name="ishellfoldersearchablefindstring-method"></a><span data-ttu-id="af61e-103">Metodo IShellFolderSearchable:: FindString</span><span class="sxs-lookup"><span data-stu-id="af61e-103">IShellFolderSearchable::FindString method</span></span>

<span data-ttu-id="af61e-104">Inizia una ricerca di una stringa di ricerca specificata.</span><span class="sxs-lookup"><span data-stu-id="af61e-104">Begins a search for a specified search string.</span></span>

## <a name="syntax"></a><span data-ttu-id="af61e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af61e-105">Syntax</span></span>


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="af61e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="af61e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af61e-107">*pwszTarget* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af61e-107">*pwszTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af61e-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="af61e-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="af61e-109">Puntatore a una stringa che specifica la parola chiave search.</span><span class="sxs-lookup"><span data-stu-id="af61e-109">A pointer to a string that specifies the search keyword.</span></span>

</dd> <dt>

<span data-ttu-id="af61e-110">*pdwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af61e-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af61e-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="af61e-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="af61e-112">Nessun flag attualmente definito. impostare su _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="af61e-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="af61e-113">*punkOnAsyncSearch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af61e-113">*punkOnAsyncSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af61e-114">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="af61e-114">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="af61e-115">Puntatore a un oggetto di tipo [_ *IUnknown* \*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="af61e-115">A pointer to an object of type [_ *IUnknown*\*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="af61e-116">Questo oggetto deve supportare l'interfaccia [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="af61e-116">This object must support the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface.</span></span> <span data-ttu-id="af61e-117">Impostare su **null** se non è necessario alcun callback.</span><span class="sxs-lookup"><span data-stu-id="af61e-117">Set to **NULL** if no callback is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="af61e-118">*ppidlOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="af61e-118">*ppidlOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af61e-119">Tipo: **LPITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="af61e-119">Type: **LPITEMIDLIST**</span></span>

<span data-ttu-id="af61e-120">Puntatore a una struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la cartella di ricerca.</span><span class="sxs-lookup"><span data-stu-id="af61e-120">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af61e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af61e-121">Return value</span></span>

<span data-ttu-id="af61e-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="af61e-122">Type: **HRESULT**</span></span>

<span data-ttu-id="af61e-123">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="af61e-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af61e-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af61e-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af61e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af61e-125">Requirements</span></span>



| <span data-ttu-id="af61e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="af61e-126">Requirement</span></span> | <span data-ttu-id="af61e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="af61e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af61e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af61e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="af61e-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="af61e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="af61e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af61e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="af61e-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="af61e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="af61e-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af61e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="af61e-133"><dt>MMC. h</dt></span><span class="sxs-lookup"><span data-stu-id="af61e-133"><dt>Mmc.h</dt></span></span> </dl>       |
| <span data-ttu-id="af61e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="af61e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af61e-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af61e-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
