---
description: Indica che una ricerca è stata completata.
title: Metodo IShellFolderSearchableCallback::RunEnd
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
ms.openlocfilehash: c23d461fdbd175a80a8fa94fcc238f6cf2f89869
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842822"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="b2c42-103">Metodo IShellFolderSearchableCallback::RunEnd</span><span class="sxs-lookup"><span data-stu-id="b2c42-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="b2c42-104">Indica che una ricerca è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b2c42-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c42-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2c42-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="b2c42-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2c42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c42-107">*dwReserved* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b2c42-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c42-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b2c42-108">Type: **DWORD**</span></span>

<span data-ttu-id="b2c42-109">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b2c42-109">Reserved.</span></span> <span data-ttu-id="b2c42-110">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="b2c42-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c42-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2c42-111">Return value</span></span>

<span data-ttu-id="b2c42-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b2c42-112">Type: **HRESULT**</span></span>

<span data-ttu-id="b2c42-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b2c42-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2c42-114">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b2c42-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c42-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2c42-115">Requirements</span></span>



| <span data-ttu-id="b2c42-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2c42-116">Requirement</span></span> | <span data-ttu-id="b2c42-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b2c42-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c42-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2c42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c42-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b2c42-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b2c42-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2c42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c42-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b2c42-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b2c42-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b2c42-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2c42-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2c42-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




