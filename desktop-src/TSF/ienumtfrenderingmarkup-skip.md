---
title: Metodo Skip IEnumTfRenderingMarkup
description: Il metodo IEnumTfRenderingMarkup Skip ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Ignora Framework servizi di testo del metodo
- Skip Method Text Services Framework, interfaccia IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup Interface Text Services Framework, Skip (metodo)
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718172"
---
# <a name="ienumtfrenderingmarkupskip-method"></a><span data-ttu-id="413a1-106">Metodo IEnumTfRenderingMarkup:: Skip</span><span class="sxs-lookup"><span data-stu-id="413a1-106">IEnumTfRenderingMarkup::Skip method</span></span>

<span data-ttu-id="413a1-107">Il metodo **IEnumTfRenderingMarkup:: Skip** ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="413a1-107">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="413a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="413a1-108">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a><span data-ttu-id="413a1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="413a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413a1-110">*ulCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="413a1-110">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413a1-111">\[in \] specifica il numero di elementi da ignorare.</span><span class="sxs-lookup"><span data-stu-id="413a1-111">\[in\] Specifies the number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413a1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="413a1-112">Return value</span></span>

<span data-ttu-id="413a1-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="413a1-113">This method can return one of these values.</span></span>



| <span data-ttu-id="413a1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="413a1-114">Value</span></span>                                                                                   | <span data-ttu-id="413a1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="413a1-115">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="413a1-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="413a1-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="413a1-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="413a1-117">The method was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="413a1-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="413a1-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="413a1-119">Il metodo ha raggiunto la fine dell'enumerazione prima che il numero di elementi specificato possa essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="413a1-119">The method reached the end of the enumeration before the specified number of elements could be skipped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="413a1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="413a1-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="413a1-121">Questo metodo non è attualmente presente nei file di intestazione pubblici.</span><span class="sxs-lookup"><span data-stu-id="413a1-121">This method is not currently in the public header files.</span></span> <span data-ttu-id="413a1-122">Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="413a1-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 





