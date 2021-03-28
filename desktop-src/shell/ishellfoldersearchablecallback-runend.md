---
description: Indica il completamento di una ricerca.
title: 'Metodo IShellFolderSearchableCallback:: RunEnd'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: 73155e65f4b6edb4a4b4b9b0d52ab5b042fa68b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994152"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="a33f3-103">Metodo IShellFolderSearchableCallback:: RunEnd</span><span class="sxs-lookup"><span data-stu-id="a33f3-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="a33f3-104">Indica il completamento di una ricerca.</span><span class="sxs-lookup"><span data-stu-id="a33f3-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a33f3-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="a33f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a33f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33f3-107">*dwReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33f3-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f3-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a33f3-108">Type: **DWORD**</span></span>

<span data-ttu-id="a33f3-109">Riservato.</span><span class="sxs-lookup"><span data-stu-id="a33f3-109">Reserved.</span></span> <span data-ttu-id="a33f3-110">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="a33f3-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33f3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a33f3-111">Return value</span></span>

<span data-ttu-id="a33f3-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a33f3-112">Type: **HRESULT**</span></span>

<span data-ttu-id="a33f3-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a33f3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a33f3-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a33f3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33f3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a33f3-115">Requirements</span></span>



| <span data-ttu-id="a33f3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33f3-116">Requirement</span></span> | <span data-ttu-id="a33f3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a33f3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a33f3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a33f3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a33f3-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a33f3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a33f3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a33f3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a33f3-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a33f3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a33f3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a33f3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a33f3-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a33f3-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




