---
title: Metodo IConfigAsfWriter2 ResetMultiPassState
description: Il metodo ResetMultiPassState Reimposta il filtro quando viene annullato un passaggio di codifica per la pre-elaborazione prima del completamento.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Metodo ResetMultiPassState Windows Media Format
- Metodo ResetMultiPassState Windows Media Format, interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2-formato Windows Media, metodo ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399513"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a><span data-ttu-id="475c2-106">Metodo IConfigAsfWriter2:: ResetMultiPassState</span><span class="sxs-lookup"><span data-stu-id="475c2-106">IConfigAsfWriter2::ResetMultiPassState method</span></span>

<span data-ttu-id="475c2-107">Il metodo **ResetMultiPassState** Reimposta il filtro quando viene annullato un passaggio di codifica per la pre-elaborazione prima del completamento.</span><span class="sxs-lookup"><span data-stu-id="475c2-107">The **ResetMultiPassState** method resets the filter when a preprocessing encoding pass is canceled before it is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="475c2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="475c2-108">Syntax</span></span>


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a><span data-ttu-id="475c2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="475c2-109">Parameters</span></span>

<span data-ttu-id="475c2-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="475c2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="475c2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="475c2-111">Return value</span></span>

<span data-ttu-id="475c2-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="475c2-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="475c2-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="475c2-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="475c2-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="475c2-114">Return code</span></span>                                                                                         | <span data-ttu-id="475c2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="475c2-115">Description</span></span>                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="475c2-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="475c2-116"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="475c2-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="475c2-117">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="475c2-118"><dt>**VFW \_ E \_ non \_ arrestato**</dt></span><span class="sxs-lookup"><span data-stu-id="475c2-118"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="475c2-119">Il filtro non si trova in uno stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="475c2-119">The filter was not in a stopped state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="475c2-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="475c2-120">Remarks</span></span>

<span data-ttu-id="475c2-121">Questo metodo deve essere chiamato per reimpostare lo stato interno del filtro ogni volta che viene annullato un passaggio di codifica per la pre-elaborazione prima che il filtro riceva un evento di **\_ \_ completamento della pre-elaborazione EC** .</span><span class="sxs-lookup"><span data-stu-id="475c2-121">This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an **EC\_PREPROCESS\_COMPLETE** event.</span></span> <span data-ttu-id="475c2-122">Non è necessario chiamare questo metodo se il passaggio di codifica per la pre-elaborazione viene completato senza errori.</span><span class="sxs-lookup"><span data-stu-id="475c2-122">It is not necessary to call this method if the preprocessing encoding pass completes without errors.</span></span>

## <a name="see-also"></a><span data-ttu-id="475c2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="475c2-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="475c2-124">[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="475c2-124">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

