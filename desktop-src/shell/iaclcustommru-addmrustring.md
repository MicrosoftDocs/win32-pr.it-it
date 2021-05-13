---
description: Aggiunge una voce all'elenco MRU (Most Recently Used).
title: Metodo IACLCustomMRU::AddMRUString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842002"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="3191e-103">Metodo IACLCustomMRU::AddMRUString</span><span class="sxs-lookup"><span data-stu-id="3191e-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="3191e-104">Aggiunge una voce all'elenco MRU (Most Recently Used).</span><span class="sxs-lookup"><span data-stu-id="3191e-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3191e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3191e-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="3191e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3191e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3191e-107">*pwszEntry* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3191e-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3191e-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3191e-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3191e-109">Puntatore a un buffer contenente la nuova voce.</span><span class="sxs-lookup"><span data-stu-id="3191e-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3191e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3191e-110">Return value</span></span>

<span data-ttu-id="3191e-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3191e-111">Type: **HRESULT**</span></span>

<span data-ttu-id="3191e-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3191e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3191e-113">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="3191e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3191e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3191e-114">Requirements</span></span>



| <span data-ttu-id="3191e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3191e-115">Requirement</span></span> | <span data-ttu-id="3191e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3191e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3191e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3191e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3191e-118">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3191e-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3191e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3191e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3191e-120">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3191e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




