---
title: Metodo Next di IEnumTfRenderingMarkup
description: Il metodo successivo IEnumTfRenderingMarkup ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Framework dei servizi di testo del metodo successivo
- Next Method Text Services Framework, interfaccia IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup Interface Text Services Framework, metodo Next
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046993"
---
# <a name="ienumtfrenderingmarkupnext-method"></a><span data-ttu-id="1adfa-106">IEnumTfRenderingMarkup:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="1adfa-106">IEnumTfRenderingMarkup::Next method</span></span>

<span data-ttu-id="1adfa-107">Il metodo **IEnumTfRenderingMarkup:: Next** ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1adfa-107">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1adfa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1adfa-108">Syntax</span></span>


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="1adfa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1adfa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1adfa-110">*ulCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1adfa-110">*ulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1adfa-111">\[out \] specifica il numero di elementi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="1adfa-111">\[out\] Specifies the number of elements to obtain.</span></span>

</dd> <dt>

<span data-ttu-id="1adfa-112">*ppElement* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1adfa-112">*ppElement* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1adfa-113">\[\]puntatore out a una matrice di strutture [tf \_ RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="1adfa-113">\[out\] Pointer to an array of [TF\_RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) structures.</span></span> <span data-ttu-id="1adfa-114">La dimensione della matrice deve essere almeno di elementi *ulCount* .</span><span class="sxs-lookup"><span data-stu-id="1adfa-114">This array must be at least *ulCount* elements in size.</span></span>

</dd> <dt>

<span data-ttu-id="1adfa-115">*pcFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1adfa-115">*pcFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1adfa-116">\[\]puntatore out a un valore ULONG che riceve il numero di elementi effettivamente ottenuti.</span><span class="sxs-lookup"><span data-stu-id="1adfa-116">\[out\] Pointer to a ULONG value that receives the number of elements actually obtained.</span></span> <span data-ttu-id="1adfa-117">Questo valore può essere minore del numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="1adfa-117">This value can be less than the number of items requested.</span></span> <span data-ttu-id="1adfa-118">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1adfa-118">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1adfa-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1adfa-119">Return value</span></span>

<span data-ttu-id="1adfa-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="1adfa-120">This method can return one of these values.</span></span>



| <span data-ttu-id="1adfa-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1adfa-121">Value</span></span>                                                                                        | <span data-ttu-id="1adfa-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1adfa-122">Description</span></span>                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1adfa-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1adfa-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1adfa-124">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="1adfa-124">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="1adfa-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1adfa-125"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="1adfa-126">Il metodo ha raggiunto la fine dell'enumerazione prima che sia possibile ottenere il numero specificato di elementi.</span><span class="sxs-lookup"><span data-stu-id="1adfa-126">The method reached the end of the enumeration before the specified number of elements could be obtained.</span></span><br/> |
| <dl> <span data-ttu-id="1adfa-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1adfa-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1adfa-128">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="1adfa-128">One or more parameters are invalid.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="1adfa-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="1adfa-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1adfa-130">Questo metodo non è attualmente presente nei file di intestazione pubblici.</span><span class="sxs-lookup"><span data-stu-id="1adfa-130">This method is not currently in the public header files.</span></span> <span data-ttu-id="1adfa-131">Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="1adfa-131">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

