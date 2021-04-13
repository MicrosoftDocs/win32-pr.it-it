---
title: Metodo IConfigAsfWriter2 StreamNumFromPin
description: Il metodo StreamNumFromPin Recupera il numero di flusso associato al pin di input specificato.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Metodo StreamNumFromPin Windows Media Format
- Metodo StreamNumFromPin Windows Media Format, interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2-formato Windows Media, metodo StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399161"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a><span data-ttu-id="71d7d-106">Metodo IConfigAsfWriter2:: StreamNumFromPin</span><span class="sxs-lookup"><span data-stu-id="71d7d-106">IConfigAsfWriter2::StreamNumFromPin method</span></span>

<span data-ttu-id="71d7d-107">Il metodo **StreamNumFromPin** Recupera il numero di flusso associato al pin di input specificato.</span><span class="sxs-lookup"><span data-stu-id="71d7d-107">The **StreamNumFromPin** method retrieves the stream number associated with the specified input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d7d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71d7d-108">Syntax</span></span>


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a><span data-ttu-id="71d7d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="71d7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d7d-110">*pPin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71d7d-110">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d7d-111">Puntatore all'interfaccia **Ipin** sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="71d7d-111">Pointer to the **IPin** interface on the input pin.</span></span>

</dd> <dt>

<span data-ttu-id="71d7d-112">*pwStreamNum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="71d7d-112">*pwStreamNum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71d7d-113">Puntatore che riceve il numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="71d7d-113">Pointer that receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d7d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71d7d-114">Return value</span></span>

<span data-ttu-id="71d7d-115">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="71d7d-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="71d7d-116">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71d7d-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d7d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="71d7d-117">Remarks</span></span>

<span data-ttu-id="71d7d-118">In alcuni casi potrebbe essere necessario usare direttamente le interfacce SDK di formato Windows Media per modificare un flusso prima di eseguire un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="71d7d-118">Sometimes you may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running a filter graph.</span></span> <span data-ttu-id="71d7d-119">Poiché non è possibile presupporre che un numero di flusso ASF corrisponda al numero del pin DirectShow, viene fornito questo metodo.</span><span class="sxs-lookup"><span data-stu-id="71d7d-119">Because you cannot assume that an ASF stream number is the same as the DirectShow pin number, this method is provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="71d7d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71d7d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="71d7d-121">[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71d7d-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

 