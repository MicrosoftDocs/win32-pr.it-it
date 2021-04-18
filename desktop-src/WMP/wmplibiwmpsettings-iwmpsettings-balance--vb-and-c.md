---
title: Proprietà Balance IWMPSettings
description: La proprietà Balance Ottiene o imposta il saldo stereo corrente.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Proprietà bilancia Media Player di Windows
- Proprietà Balance Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Media Player Windows, Balance (proprietà)
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330447"
---
# <a name="iwmpsettingsbalance-property"></a><span data-ttu-id="233ad-106">Proprietà IWMPSettings:: Balance</span><span class="sxs-lookup"><span data-stu-id="233ad-106">IWMPSettings::balance property</span></span>

<span data-ttu-id="233ad-107">La proprietà **Balance** Ottiene o imposta il saldo stereo corrente.</span><span class="sxs-lookup"><span data-stu-id="233ad-107">The **balance** property gets or sets the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="233ad-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="233ad-108">Syntax</span></span>


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="233ad-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="233ad-109">Property value</span></span>

<span data-ttu-id="233ad-110">**System. Int32** che rappresenta il valore di bilanciamento.</span><span class="sxs-lookup"><span data-stu-id="233ad-110">A **System.Int32** that is the balance value.</span></span> <span data-ttu-id="233ad-111">Questo valore può essere compreso tra 100 e 100.</span><span class="sxs-lookup"><span data-stu-id="233ad-111">This value can range from  100 to 100.</span></span> <span data-ttu-id="233ad-112">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="233ad-112">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="233ad-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="233ad-113">Remarks</span></span>

<span data-ttu-id="233ad-114">Il valore zero indica che l'audio viene riprodotto in un volume uguale sui canali sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="233ad-114">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="233ad-115">Il valore 100 indica che l'audio viene riprodotto solo sul canale sinistro.</span><span class="sxs-lookup"><span data-stu-id="233ad-115">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="233ad-116">Il valore 100 indica che l'audio viene riprodotto solo sul canale destro.</span><span class="sxs-lookup"><span data-stu-id="233ad-116">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="233ad-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="233ad-117">Requirements</span></span>



| <span data-ttu-id="233ad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="233ad-118">Requirement</span></span> | <span data-ttu-id="233ad-119">Valore</span><span class="sxs-lookup"><span data-stu-id="233ad-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="233ad-120">Versione</span><span class="sxs-lookup"><span data-stu-id="233ad-120">Version</span></span><br/>   | <span data-ttu-id="233ad-121">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="233ad-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="233ad-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="233ad-122">Namespace</span></span><br/> | <span data-ttu-id="233ad-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="233ad-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="233ad-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="233ad-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="233ad-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="233ad-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="233ad-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="233ad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233ad-127">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="233ad-127">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





