---
title: Metodo gratuito IMemoryAllocator
description: Il metodo Free libera la memoria allocata dal metodo allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Archiviazione strutturata metodo gratuito
- Archiviazione strutturata di metodi gratuiti, interfaccia IMemoryAllocator
- Archiviazione strutturata dell'interfaccia IMemoryAllocator, metodo gratuito
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047962"
---
# <a name="imemoryallocatorfree-method"></a><span data-ttu-id="1285f-106">Metodo IMemoryAllocator:: Free</span><span class="sxs-lookup"><span data-stu-id="1285f-106">IMemoryAllocator::Free method</span></span>

<span data-ttu-id="1285f-107">Il metodo **Free** libera la memoria allocata dal metodo [**allocate**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="1285f-107">The **Free** method frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1285f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1285f-108">Syntax</span></span>


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a><span data-ttu-id="1285f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1285f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1285f-110">*PV*</span><span class="sxs-lookup"><span data-stu-id="1285f-110">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="1285f-111">Puntatore alla memoria da liberare.</span><span class="sxs-lookup"><span data-stu-id="1285f-111">Pointer to the memory to be freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1285f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1285f-112">Requirements</span></span>



| <span data-ttu-id="1285f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1285f-113">Requirement</span></span> | <span data-ttu-id="1285f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1285f-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1285f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1285f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1285f-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1285f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1285f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1285f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1285f-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1285f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1285f-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="1285f-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="1285f-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1285f-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

 





