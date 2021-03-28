---
description: Ottiene il nome della visualizzazione predefinita. Chiamare GetDisplayNameOf per recuperare i nomi delle altre visualizzazioni.
title: 'Metodo IShellFolderViewType:: GetDefaultViewName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977938"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="acbe0-104">Metodo IShellFolderViewType:: GetDefaultViewName</span><span class="sxs-lookup"><span data-stu-id="acbe0-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="acbe0-105">Ottiene il nome della visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="acbe0-105">Gets the name of the default view.</span></span> <span data-ttu-id="acbe0-106">Chiamare [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per recuperare i nomi delle altre visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="acbe0-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="acbe0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acbe0-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="acbe0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="acbe0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acbe0-109">*uFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="acbe0-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acbe0-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="acbe0-110">Type: **DWORD**</span></span>

<span data-ttu-id="acbe0-111">Flag facoltativi; deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="acbe0-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="acbe0-112">*ppwszName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="acbe0-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acbe0-113">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="acbe0-113">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="acbe0-114">Indirizzo di un puntatore di stringa che riceve il nome della visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="acbe0-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="acbe0-115">La memoria per la stringa viene allocata con [_ *SHStrDup* \*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span><span class="sxs-lookup"><span data-stu-id="acbe0-115">The memory for the string is allocated with [_ *SHStrDup*\*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acbe0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="acbe0-116">Return value</span></span>

<span data-ttu-id="acbe0-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="acbe0-117">Type: **HRESULT**</span></span>

<span data-ttu-id="acbe0-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="acbe0-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="acbe0-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="acbe0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="acbe0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acbe0-120">Requirements</span></span>



| <span data-ttu-id="acbe0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="acbe0-121">Requirement</span></span> | <span data-ttu-id="acbe0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="acbe0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="acbe0-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acbe0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="acbe0-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="acbe0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="acbe0-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acbe0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="acbe0-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="acbe0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="acbe0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="acbe0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acbe0-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acbe0-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




