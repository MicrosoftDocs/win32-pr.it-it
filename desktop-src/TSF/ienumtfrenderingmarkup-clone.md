---
title: Metodo Clone IEnumTfRenderingMarkup
description: Il metodo Clone IEnumTfRenderingMarkup crea una copia dell'oggetto enumeratore.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Framework dei servizi di testo del metodo Clone
- Framework dei servizi di testo del metodo Clone, interfaccia IEnumTfRenderingMarkup
- Framework dei servizi di testo dell'interfaccia IEnumTfRenderingMarkup, metodo Clone
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299962"
---
# <a name="ienumtfrenderingmarkupclone-method"></a><span data-ttu-id="75ca9-106">Metodo IEnumTfRenderingMarkup:: Clone</span><span class="sxs-lookup"><span data-stu-id="75ca9-106">IEnumTfRenderingMarkup::Clone method</span></span>

<span data-ttu-id="75ca9-107">Il metodo **IEnumTfRenderingMarkup:: Clone** crea una copia dell'oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="75ca9-107">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ca9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75ca9-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="75ca9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="75ca9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ca9-110">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="75ca9-110">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75ca9-111">\[\]un puntatore a un'interfaccia [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="75ca9-111">\[out\] A pointer to a [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ca9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75ca9-112">Return value</span></span>

<span data-ttu-id="75ca9-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="75ca9-113">This method can return one of these values.</span></span>



| <span data-ttu-id="75ca9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="75ca9-114">Value</span></span>                                                                                        | <span data-ttu-id="75ca9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75ca9-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="75ca9-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="75ca9-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="75ca9-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="75ca9-117">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="75ca9-118"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="75ca9-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="75ca9-119">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="75ca9-119">An unspecified error occurred.</span></span><br/>      |
| <dl> <span data-ttu-id="75ca9-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="75ca9-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="75ca9-121">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="75ca9-121">One or more parameters are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75ca9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="75ca9-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="75ca9-123">Questo metodo non è attualmente presente nei file di intestazione pubblici.</span><span class="sxs-lookup"><span data-stu-id="75ca9-123">This method is not currently in the public header files.</span></span> <span data-ttu-id="75ca9-124">Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="75ca9-124">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

