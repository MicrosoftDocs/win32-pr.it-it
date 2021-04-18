---
title: IWMPDVD. disavailable (VB e C)
description: La proprietà disavailable (il \_ metodo Get disavailable in C \) ottiene un valore che indica se un tipo specificato di informazioni è disponibile o se è possibile eseguire un'azione specificata.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. disavailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330727"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a><span data-ttu-id="781a5-104">IWMPDVD. disavailable (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="781a5-104">IWMPDVD.isAvailable (VB and C#)</span></span>

<span data-ttu-id="781a5-105">La **proprietà IsValid (il** metodo **get \_ disavailable** in C#) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="781a5-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a><span data-ttu-id="781a5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="781a5-106">Parameters</span></span>

<span data-ttu-id="781a5-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="781a5-107">*bstrItem*</span></span>

<span data-ttu-id="781a5-108">System. String che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="781a5-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="781a5-109">Valore</span><span class="sxs-lookup"><span data-stu-id="781a5-109">Value</span></span>      | <span data-ttu-id="781a5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="781a5-110">Description</span></span>                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="781a5-111">Indietro</span><span class="sxs-lookup"><span data-stu-id="781a5-111">back</span></span>       | <span data-ttu-id="781a5-112">Individua se è disponibile il metodo **IWMPDVD. back** .</span><span class="sxs-lookup"><span data-stu-id="781a5-112">Discovers whether the **IWMPDVD.back** method is available.</span></span>                                   |
| <span data-ttu-id="781a5-113">DVD</span><span class="sxs-lookup"><span data-stu-id="781a5-113">dvd</span></span>        | <span data-ttu-id="781a5-114">Rileva se il DVD è caricato.</span><span class="sxs-lookup"><span data-stu-id="781a5-114">Discovers whether the DVD is loaded.</span></span>                                                          |
| <span data-ttu-id="781a5-115">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="781a5-115">dvdDecoder</span></span> | <span data-ttu-id="781a5-116">Rileva se il decoder DVD è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="781a5-116">Discovers whether the DVD decoder is installed on system.</span></span>                                     |
| <span data-ttu-id="781a5-117">resume</span><span class="sxs-lookup"><span data-stu-id="781a5-117">resume</span></span>     | <span data-ttu-id="781a5-118">Rileva se il metodo **IWMPDVD. Resume** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="781a5-118">Discovers whether the **IWMPDVD.resume** method is available.</span></span>                                 |
| <span data-ttu-id="781a5-119">titleMenu</span><span class="sxs-lookup"><span data-stu-id="781a5-119">titleMenu</span></span>  | <span data-ttu-id="781a5-120">Rileva se il metodo **IWMPDVD. titleMenu** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="781a5-120">Discovers whether the **IWMPDVD.titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="781a5-121">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="781a5-121">topMenu</span></span>    | <span data-ttu-id="781a5-122">Rileva se il metodo **IWMPDVD. tomenu** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="781a5-122">Discovers whether the **IWMPDVD.topMenu** method is available.</span></span> <span data-ttu-id="781a5-123">Comunemente chiamato menu radice.</span><span class="sxs-lookup"><span data-stu-id="781a5-123">Commonly called the root menu.</span></span> |



 

## <a name="property-value"></a><span data-ttu-id="781a5-124">Valore della proprietà</span><span class="sxs-lookup"><span data-stu-id="781a5-124">Property Value</span></span>

<span data-ttu-id="781a5-125">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="781a5-125">**System.Boolean**</span></span>

<span data-ttu-id="781a5-126">**System. Boolean** che indica se un tipo specificato di informazioni è disponibile o se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="781a5-126">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="781a5-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="781a5-127">Remarks</span></span>

<span data-ttu-id="781a5-128">Le funzionalità DVD di Windows Media Player non funzioneranno nei computer in cui non è installato un decoder DVD.</span><span class="sxs-lookup"><span data-stu-id="781a5-128">The DVD features of Windows Media Player will not work on computers that do not have a DVD decoder installed.</span></span> <span data-ttu-id="781a5-129">È possibile determinare se un decodificatore è disponibile chiamando la proprietà **disavailable** (il metodo **get \_ disavailable** in C#) e passando il valore **System. String** "dvdDecoder".</span><span class="sxs-lookup"><span data-stu-id="781a5-129">You can determine whether a decoder is available by calling the **isAvailable** property (the **get\_isAvailable** method in C#) and passing in the **System.String** value "dvdDecoder".</span></span>

<span data-ttu-id="781a5-130">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="781a5-130">Every DVD is authored differently.</span></span> <span data-ttu-id="781a5-131">I metodi disponibili durante la riproduzione e la navigazione in DVD dipendono dal modo in cui viene creato il DVD.</span><span class="sxs-lookup"><span data-stu-id="781a5-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

## <a name="requirements"></a><span data-ttu-id="781a5-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="781a5-132">Requirements</span></span>



| <span data-ttu-id="781a5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="781a5-133">Requirement</span></span> | <span data-ttu-id="781a5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="781a5-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="781a5-135">Versione</span><span class="sxs-lookup"><span data-stu-id="781a5-135">Version</span></span><br/>   | <span data-ttu-id="781a5-136">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="781a5-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="781a5-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="781a5-137">Namespace</span></span><br/> | <span data-ttu-id="781a5-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="781a5-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="781a5-139">Assembly</span><span class="sxs-lookup"><span data-stu-id="781a5-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="781a5-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="781a5-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="781a5-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="781a5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781a5-142">**Interfaccia IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="781a5-142">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="781a5-143">**IWMPDVD. Back (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="781a5-143">**IWMPDVD.back (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="781a5-144">**IWMPDVD. Resume (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="781a5-144">**IWMPDVD.resume (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="781a5-145">**IWMPDVD. titleMenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="781a5-145">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="781a5-146">**IWMPDVD. tomenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="781a5-146">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





