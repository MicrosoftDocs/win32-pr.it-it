---
title: IWMPControls. disavailable (VB e C)
description: La proprietà disavailable (il \_ metodo Get disavailable in C \) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. disavailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328213"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a><span data-ttu-id="3680a-104">IWMPControls. disavailable (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="3680a-104">IWMPControls.isAvailable (VB and C#)</span></span>

<span data-ttu-id="3680a-105">La proprietà **disavailable** (il metodo **get \_ disavailable** in C#) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="3680a-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="3680a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3680a-106">Parameters</span></span>

<span data-ttu-id="3680a-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="3680a-107">*bstrItem*</span></span>

<span data-ttu-id="3680a-108">System. String che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3680a-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="3680a-109">Valore</span><span class="sxs-lookup"><span data-stu-id="3680a-109">Value</span></span>           | <span data-ttu-id="3680a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3680a-110">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3680a-111">currentItem</span><span class="sxs-lookup"><span data-stu-id="3680a-111">currentItem</span></span>     | <span data-ttu-id="3680a-112">Individua se l'utente può impostare la proprietà **IWMPControls. CurrentItem** .</span><span class="sxs-lookup"><span data-stu-id="3680a-112">Discovers whether the user can set the **IWMPControls.currentItem** property.</span></span>                                                                                     |
| <span data-ttu-id="3680a-113">currentMarker</span><span class="sxs-lookup"><span data-stu-id="3680a-113">currentMarker</span></span>   | <span data-ttu-id="3680a-114">Individua se l'utente può cercare un marcatore specifico.</span><span class="sxs-lookup"><span data-stu-id="3680a-114">Discovers whether the user can seek to a specific marker.</span></span>                                                                                                         |
| <span data-ttu-id="3680a-115">currentPosition</span><span class="sxs-lookup"><span data-stu-id="3680a-115">currentPosition</span></span> | <span data-ttu-id="3680a-116">Individua se l'utente può eseguire la ricerca in una posizione specifica nel file.</span><span class="sxs-lookup"><span data-stu-id="3680a-116">Discovers whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="3680a-117">Alcuni file non supportano la ricerca.</span><span class="sxs-lookup"><span data-stu-id="3680a-117">Some files do not support seeking.</span></span>                                                        |
| <span data-ttu-id="3680a-118">fastForward</span><span class="sxs-lookup"><span data-stu-id="3680a-118">fastForward</span></span>     | <span data-ttu-id="3680a-119">Rileva se il file supporta l'avanzamento rapido e se tale funzionalità può essere richiamata.</span><span class="sxs-lookup"><span data-stu-id="3680a-119">Discovers whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="3680a-120">Molti tipi di file (e flussi live) non supportano fastForward.</span><span class="sxs-lookup"><span data-stu-id="3680a-120">Many file types (and live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="3680a-121">fastReverse</span><span class="sxs-lookup"><span data-stu-id="3680a-121">fastReverse</span></span>     | <span data-ttu-id="3680a-122">Rileva se il file supporta fastReverse e se tale funzionalità può essere richiamata.</span><span class="sxs-lookup"><span data-stu-id="3680a-122">Discovers whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="3680a-123">Molti tipi di file (e flussi live) non supportano fastReverse.</span><span class="sxs-lookup"><span data-stu-id="3680a-123">Many file types (and live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="3680a-124">Avanti</span><span class="sxs-lookup"><span data-stu-id="3680a-124">next</span></span>            | <span data-ttu-id="3680a-125">Individua se l'utente può cercare la voce successiva in una playlist.</span><span class="sxs-lookup"><span data-stu-id="3680a-125">Discovers whether the user can seek to the next entry in a playlist.</span></span>                                                                                              |
| <span data-ttu-id="3680a-126">Sospendi</span><span class="sxs-lookup"><span data-stu-id="3680a-126">pause</span></span>           | <span data-ttu-id="3680a-127">Individua se è disponibile il metodo **IWMPControls. pause** .</span><span class="sxs-lookup"><span data-stu-id="3680a-127">Discovers whether the **IWMPControls.pause** method is available.</span></span>                                                                                                 |
| <span data-ttu-id="3680a-128">Play</span><span class="sxs-lookup"><span data-stu-id="3680a-128">play</span></span>            | <span data-ttu-id="3680a-129">Rileva se il metodo **IWMPControls. Play** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3680a-129">Discovers whether the **IWMPControls.play** method is available.</span></span>                                                                                                  |
| <span data-ttu-id="3680a-130">previous</span><span class="sxs-lookup"><span data-stu-id="3680a-130">previous</span></span>        | <span data-ttu-id="3680a-131">Individua se l'utente può cercare la voce precedente in una playlist.</span><span class="sxs-lookup"><span data-stu-id="3680a-131">Discovers whether the user can seek to the previous entry in a playlist.</span></span>                                                                                          |
| <span data-ttu-id="3680a-132">step</span><span class="sxs-lookup"><span data-stu-id="3680a-132">step</span></span>            | <span data-ttu-id="3680a-133">Rileva se il metodo **IWMPControls2. Step** è disponibile durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3680a-133">Discovers whether the **IWMPControls2.step** method is available during playback.</span></span>                                                                                 |
| <span data-ttu-id="3680a-134">stop</span><span class="sxs-lookup"><span data-stu-id="3680a-134">stop</span></span>            | <span data-ttu-id="3680a-135">Rileva se il metodo **IWMPControls. Stop** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3680a-135">Discovers whether the **IWMPControls.stop** method is available.</span></span>                                                                                                  |



 

## <a name="property-value"></a><span data-ttu-id="3680a-136">Valore della proprietà</span><span class="sxs-lookup"><span data-stu-id="3680a-136">Property Value</span></span>

<span data-ttu-id="3680a-137">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="3680a-137">**System.Boolean**</span></span>

<span data-ttu-id="3680a-138">**System. Boolean** che indica se un tipo specificato di informazioni è disponibile o se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="3680a-138">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="3680a-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="3680a-139">Remarks</span></span>

<span data-ttu-id="3680a-140">**IWMPControls. disavailable** è una proprietà in Visual Basic che accetta un parametro.</span><span class="sxs-lookup"><span data-stu-id="3680a-140">**IWMPControls.isAvailable** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="3680a-141">In C# viene indicato come il metodo **IWMPControls. Get \_ unavailable** .</span><span class="sxs-lookup"><span data-stu-id="3680a-141">In C# it is referred to as the **IWMPControls.get\_isAvailable** method.</span></span>

## <a name="examples"></a><span data-ttu-id="3680a-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="3680a-142">Examples</span></span>

<span data-ttu-id="3680a-143">Nell'esempio seguente viene utilizzata **la proprietà IsValid** (il metodo **get \_ disavailable** in C#) per verificare che l'elemento multimediale corrente supporti la proprietà **currentPosition** .</span><span class="sxs-lookup"><span data-stu-id="3680a-143">The following example uses the **isAvailable** property (the **get\_isAvailable** method in C#) to verify that the current media item supports the **currentPosition** property.</span></span> <span data-ttu-id="3680a-144">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="3680a-144">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a><span data-ttu-id="3680a-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3680a-145">Requirements</span></span>



| <span data-ttu-id="3680a-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3680a-146">Requirement</span></span> | <span data-ttu-id="3680a-147">Valore</span><span class="sxs-lookup"><span data-stu-id="3680a-147">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3680a-148">Versione</span><span class="sxs-lookup"><span data-stu-id="3680a-148">Version</span></span><br/>   | <span data-ttu-id="3680a-149">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3680a-149">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3680a-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3680a-150">Namespace</span></span><br/> | <span data-ttu-id="3680a-151">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3680a-151">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3680a-152">Assembly</span><span class="sxs-lookup"><span data-stu-id="3680a-152">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3680a-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3680a-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3680a-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3680a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3680a-155">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3680a-155">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3680a-156">**IWMPControls. currentItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3680a-156">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3680a-157">**IWMPControls. pause (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3680a-157">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3680a-158">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3680a-158">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3680a-159">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3680a-159">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3680a-160">**IWMPControls2. Step (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3680a-160">**IWMPControls2.step (VB and C#)**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





