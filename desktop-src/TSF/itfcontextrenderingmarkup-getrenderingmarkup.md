---
title: Metodo ITfContextRenderingMarkup GetRenderingMarkup
description: Il metodo ITfContextRenderingMarkup GetRenderingMarkup recupera un enumeratore dei markup di rendering per l'intervallo specificato.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Framework servizi di testo Metodo GetRenderingMarkup
- Framework dei servizi di testo del metodo GetRenderingMarkup, interfaccia ITfContextRenderingMarkup
- ITfContextRenderingMarkup Interface Text Services Framework, metodo GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728554"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a><span data-ttu-id="99461-106">Metodo ITfContextRenderingMarkup:: GetRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="99461-106">ITfContextRenderingMarkup::GetRenderingMarkup method</span></span>

<span data-ttu-id="99461-107">Il metodo **ITfContextRenderingMarkup:: GetRenderingMarkup** recupera un enumeratore dei markup di rendering per l'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="99461-107">The **ITfContextRenderingMarkup::GetRenderingMarkup** method retrieves an enumerator of the rendering markups for the given range.</span></span>

## <a name="syntax"></a><span data-ttu-id="99461-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99461-108">Syntax</span></span>


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="99461-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="99461-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99461-110">*EC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99461-110">*ec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99461-111">\[in \] un cookie di modifica di sola lettura per accedere al contesto.</span><span class="sxs-lookup"><span data-stu-id="99461-111">\[in\] A read only edit cookie to access the context.</span></span>

</dd> <dt>

<span data-ttu-id="99461-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99461-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99461-113">\[in\]</span><span class="sxs-lookup"><span data-stu-id="99461-113">\[in\]</span></span>



| <span data-ttu-id="99461-114">Valore</span><span class="sxs-lookup"><span data-stu-id="99461-114">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="99461-115">Significato</span><span class="sxs-lookup"><span data-stu-id="99461-115">Meaning</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <span data-ttu-id="99461-116"><dt>**\_proprietà di \_ inclusione TF GRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99461-116"><dt>**TF\_GRM\_INCLUDE\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="99461-117">Se questo bit è 1, l'enumeratore includerà la \_ proprietà dell'attributo GUID Prop \_ .</span><span class="sxs-lookup"><span data-stu-id="99461-117">If this bit is 1, the enumerator will include the GUID\_PROP\_ATTRIBUTE property.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="99461-118">*pRangeCover* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99461-118">*pRangeCover* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99461-119">\[in \] un puntatore a un'interfaccia [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) dell'intervallo per enumerare i markup di rendering.</span><span class="sxs-lookup"><span data-stu-id="99461-119">\[in\] A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface of the range to enumerate the rendering markups.</span></span>

</dd> <dt>

<span data-ttu-id="99461-120">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="99461-120">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99461-121">\[\]un puntatore per recuperare il puntatore all'interfaccia [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="99461-121">\[out\] A pointer to retrieve [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99461-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99461-122">Return value</span></span>

<span data-ttu-id="99461-123">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="99461-123">This method can return one of these values.</span></span>



| <span data-ttu-id="99461-124">Valore</span><span class="sxs-lookup"><span data-stu-id="99461-124">Value</span></span>                                                                                | <span data-ttu-id="99461-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99461-125">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="99461-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="99461-126"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="99461-127">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="99461-127">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="99461-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="99461-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="99461-129">Questo metodo non è attualmente presente nei file di intestazione pubblici.</span><span class="sxs-lookup"><span data-stu-id="99461-129">This method is not currently in the public header files.</span></span> <span data-ttu-id="99461-130">Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="99461-130">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

