---
title: Metodo IWMPControls2 Step
description: Il metodo Step fa passare l'elemento del supporto video corrente al frame successivo o al frame precedente e bloccare la riproduzione.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- Metodo Step Media Player Windows
- Metodo Step Media Player Windows, interfaccia IWMPControls2
- Interfaccia IWMPControls2 Windows Media Player, Metodo Step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332468"
---
# <a name="iwmpcontrols2step-method"></a><span data-ttu-id="62f92-106">Metodo IWMPControls2:: Step</span><span class="sxs-lookup"><span data-stu-id="62f92-106">IWMPControls2::step method</span></span>

<span data-ttu-id="62f92-107">Il metodo **Step** fa passare l'elemento del supporto video corrente al frame successivo o al frame precedente e bloccare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="62f92-107">The **step** method causes the current video media item to step to the next frame or the previous frame and freeze playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f92-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62f92-108">Syntax</span></span>


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a><span data-ttu-id="62f92-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="62f92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62f92-110">*lStep* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62f92-110">*lStep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62f92-111">Valore **System. Int32** che indica il numero di frame da scorrere prima del blocco.</span><span class="sxs-lookup"><span data-stu-id="62f92-111">A **System.Int32** value indicating how many frames to step before freezing.</span></span> <span data-ttu-id="62f92-112">Deve essere impostato su 1 o-1.</span><span class="sxs-lookup"><span data-stu-id="62f92-112">Must be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62f92-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62f92-113">Return value</span></span>

<span data-ttu-id="62f92-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="62f92-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62f92-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="62f92-115">Remarks</span></span>

<span data-ttu-id="62f92-116">Questo metodo supporta attualmente solo i parametri 1 o-1, pertanto è possibile eseguire solo un passaggio di un frame alla volta.</span><span class="sxs-lookup"><span data-stu-id="62f92-116">This method currently supports only the parameters 1 or -1, so you can only step one frame at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="62f92-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62f92-117">Requirements</span></span>



| <span data-ttu-id="62f92-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f92-118">Requirement</span></span> | <span data-ttu-id="62f92-119">Valore</span><span class="sxs-lookup"><span data-stu-id="62f92-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62f92-120">Versione</span><span class="sxs-lookup"><span data-stu-id="62f92-120">Version</span></span><br/>   | <span data-ttu-id="62f92-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="62f92-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="62f92-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="62f92-122">Namespace</span></span><br/> | <span data-ttu-id="62f92-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="62f92-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="62f92-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="62f92-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="62f92-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="62f92-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62f92-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62f92-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f92-127">**Interfaccia IWMPControls2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="62f92-127">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="62f92-128">**Interfaccia IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="62f92-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





