---
title: Proprietà maxBandwidth di IWMPNetwork
description: La proprietà maxBandwidth Ottiene o imposta la larghezza di banda massima consentita.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- Finestra delle proprietà di maxBandwidth Media Player
- Proprietà di maxBandwidth Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329911"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a><span data-ttu-id="27fb3-106">Proprietà IWMPNetwork:: maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="27fb3-106">IWMPNetwork::maxBandwidth property</span></span>

<span data-ttu-id="27fb3-107">La proprietà **maxBandwidth** Ottiene o imposta la larghezza di banda massima consentita.</span><span class="sxs-lookup"><span data-stu-id="27fb3-107">The **maxBandwidth** property gets or sets the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="27fb3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27fb3-108">Syntax</span></span>


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="27fb3-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="27fb3-109">Property value</span></span>

<span data-ttu-id="27fb3-110">**System. Int32** che rappresenta la larghezza di banda massima.</span><span class="sxs-lookup"><span data-stu-id="27fb3-110">A **System.Int32** that is the maximum bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="27fb3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="27fb3-111">Remarks</span></span>

<span data-ttu-id="27fb3-112">Questa proprietà non ha un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="27fb3-112">This property does not have a default value.</span></span> <span data-ttu-id="27fb3-113">Il valore può essere specificato durante la riproduzione di Windows Media Player, ma la modifica non verrà applicata fino a quando l'elemento multimediale corrente non viene rilasciato aprendone un altro o chiamando **AxWindowsMediaPlayer. Close**.</span><span class="sxs-lookup"><span data-stu-id="27fb3-113">The value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling **AxWindowsMediaPlayer.close**.</span></span> <span data-ttu-id="27fb3-114">Windows Media Player tenta di ottenere la massima larghezza di banda possibile.</span><span class="sxs-lookup"><span data-stu-id="27fb3-114">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="27fb3-115">Non verrà eseguita alcuna riduzione intenzionale della larghezza di banda a meno che questo valore non sia impostato.</span><span class="sxs-lookup"><span data-stu-id="27fb3-115">No intentional reduction of bandwidth will occur unless this value is set.</span></span>

<span data-ttu-id="27fb3-116">Questa impostazione è utile per ridurre la quantità di larghezza di banda usata, in particolare nel caso di un flusso a più velocità in bit (MBR).</span><span class="sxs-lookup"><span data-stu-id="27fb3-116">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="27fb3-117">Un flusso MBR contiene più flussi con velocità in bit diverse.</span><span class="sxs-lookup"><span data-stu-id="27fb3-117">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="27fb3-118">In alcuni casi, può essere utile usare un flusso con una velocità in bit inferiore a quella richiesta dal client.</span><span class="sxs-lookup"><span data-stu-id="27fb3-118">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="27fb3-119">In questo caso, se si specifica una velocità in bit più bassa con la proprietà **IWMPNetwork. maxBandwidth** , verrà selezionato un flusso a velocità in bit inferiore.</span><span class="sxs-lookup"><span data-stu-id="27fb3-119">In this case, specifying a lower bit rate with the **IWMPNetwork.maxBandwidth** property will select a lower bit-rate stream.</span></span> <span data-ttu-id="27fb3-120">Ad esempio, un flusso MBR può includere flussi codificati a 20 kilobit al secondo (Kbps), 37 kbps e 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="27fb3-120">For example, an MBR stream might include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="27fb3-121">Se si usa **IWMPNetwork. maxBandwidth** per specificare una velocità in bit di 50.000 (50 Kbps), si selezionerà il flusso 37 Kbps anziché il flusso a 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="27fb3-121">Using **IWMPNetwork.maxBandwidth** to specify a bit rate of 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="27fb3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27fb3-122">Requirements</span></span>



| <span data-ttu-id="27fb3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="27fb3-123">Requirement</span></span> | <span data-ttu-id="27fb3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="27fb3-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27fb3-125">Versione</span><span class="sxs-lookup"><span data-stu-id="27fb3-125">Version</span></span><br/>   | <span data-ttu-id="27fb3-126">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="27fb3-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="27fb3-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="27fb3-127">Namespace</span></span><br/> | <span data-ttu-id="27fb3-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="27fb3-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="27fb3-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="27fb3-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="27fb3-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="27fb3-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27fb3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27fb3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27fb3-132">**AxWindowsMediaPlayer. Close (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="27fb3-132">**AxWindowsMediaPlayer.close (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="27fb3-133">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="27fb3-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





