---
description: Inizia il completamento dell'attività.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'Metodo TaskCompletionClient:: ApplyTaskCompletion'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994965"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a><span data-ttu-id="9840a-103">Metodo TaskCompletionClient:: ApplyTaskCompletion</span><span class="sxs-lookup"><span data-stu-id="9840a-103">TaskCompletionClient::ApplyTaskCompletion method</span></span>

<span data-ttu-id="9840a-104">Inizia il completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="9840a-104">Begins the task completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="9840a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9840a-105">Syntax</span></span>


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a><span data-ttu-id="9840a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9840a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9840a-107">*ptcfCategory*</span><span class="sxs-lookup"><span data-stu-id="9840a-107">*ptcfCategory*</span></span> 
</dt> <dd>

<span data-ttu-id="9840a-108">Valore che indica la categoria dell'attività.</span><span class="sxs-lookup"><span data-stu-id="9840a-108">A value indicating the category of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9840a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9840a-109">Return value</span></span>

<span data-ttu-id="9840a-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9840a-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9840a-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9840a-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9840a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9840a-112">Remarks</span></span>

<span data-ttu-id="9840a-113">L'unico valore supportato per *ptcfCategory* è 0x08000000.</span><span class="sxs-lookup"><span data-stu-id="9840a-113">The only supported value for *ptcfCategory* is 0x08000000.</span></span>

## <a name="requirements"></a><span data-ttu-id="9840a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9840a-114">Requirements</span></span>



| <span data-ttu-id="9840a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9840a-115">Requirement</span></span> | <span data-ttu-id="9840a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9840a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9840a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9840a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9840a-118">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9840a-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9840a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9840a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9840a-120">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="9840a-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9840a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9840a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9840a-122"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9840a-122"><dt>ExecModelClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9840a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9840a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9840a-124">**TaskCompletionClient**</span><span class="sxs-lookup"><span data-stu-id="9840a-124">**TaskCompletionClient**</span></span>](taskcompletionclient.md)
</dt> </dl>

 

 




