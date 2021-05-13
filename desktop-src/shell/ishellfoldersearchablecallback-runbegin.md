---
description: Indica che è stata avviata una ricerca.
title: Metodo IShellFolderSearchableCallback::RunBegin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 953bf54ff64cf41724ce0dfabd064f9c7b980cc6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842812"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a><span data-ttu-id="d27f1-103">Metodo IShellFolderSearchableCallback::RunBegin</span><span class="sxs-lookup"><span data-stu-id="d27f1-103">IShellFolderSearchableCallback::RunBegin method</span></span>

<span data-ttu-id="d27f1-104">Indica che è stata avviata una ricerca.</span><span class="sxs-lookup"><span data-stu-id="d27f1-104">Indicates that a search was started.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d27f1-105">Syntax</span></span>


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="d27f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d27f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27f1-107">*dwReserved* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d27f1-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d27f1-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d27f1-108">Type: **DWORD**</span></span>

<span data-ttu-id="d27f1-109">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d27f1-109">Reserved.</span></span> <span data-ttu-id="d27f1-110">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="d27f1-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27f1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d27f1-111">Return value</span></span>

<span data-ttu-id="d27f1-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d27f1-112">Type: **HRESULT**</span></span>

<span data-ttu-id="d27f1-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d27f1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d27f1-114">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d27f1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d27f1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d27f1-115">Remarks</span></span>

<span data-ttu-id="d27f1-116">In risposta a questo callback, l'applicazione può ad esempio abilitare **il pulsante** Annulla.</span><span class="sxs-lookup"><span data-stu-id="d27f1-116">In response to this callback, the application may enable the **Cancel** button, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="d27f1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d27f1-117">Requirements</span></span>



| <span data-ttu-id="d27f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d27f1-118">Requirement</span></span> | <span data-ttu-id="d27f1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d27f1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d27f1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d27f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d27f1-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d27f1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d27f1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d27f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d27f1-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d27f1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d27f1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d27f1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d27f1-125"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d27f1-125"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




