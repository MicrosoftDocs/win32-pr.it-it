---
title: Controls. disavailable
description: La proprietà disavailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | Controls. disavailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Media Player di Windows Controls. available
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330006"
---
# <a name="controlsisavailable"></a><span data-ttu-id="917f1-105">Controls. disavailable</span><span class="sxs-lookup"><span data-stu-id="917f1-105">Controls.isAvailable</span></span>

<span data-ttu-id="917f1-106">La proprietà **disavailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="917f1-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="917f1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="917f1-107">Parameters</span></span>

<span data-ttu-id="917f1-108">*nome*</span><span class="sxs-lookup"><span data-stu-id="917f1-108">*name*</span></span>

<span data-ttu-id="917f1-109">**Stringa** contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="917f1-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="917f1-110">string</span><span class="sxs-lookup"><span data-stu-id="917f1-110">String</span></span>          | <span data-ttu-id="917f1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="917f1-111">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="917f1-112">currentItem</span><span class="sxs-lookup"><span data-stu-id="917f1-112">currentItem</span></span>     | <span data-ttu-id="917f1-113">Determina se l'utente può impostare la proprietà **CurrentItem** .</span><span class="sxs-lookup"><span data-stu-id="917f1-113">Determines whether the user can set the **currentItem** property.</span></span>                                                                                                 |
| <span data-ttu-id="917f1-114">currentMarker</span><span class="sxs-lookup"><span data-stu-id="917f1-114">currentMarker</span></span>   | <span data-ttu-id="917f1-115">Determina se l'utente può cercare un marcatore specifico.</span><span class="sxs-lookup"><span data-stu-id="917f1-115">Determines whether the user can seek to a specific marker.</span></span>                                                                                                        |
| <span data-ttu-id="917f1-116">currentPosition</span><span class="sxs-lookup"><span data-stu-id="917f1-116">currentPosition</span></span> | <span data-ttu-id="917f1-117">Determina se l'utente può eseguire la ricerca in una posizione specifica nel file.</span><span class="sxs-lookup"><span data-stu-id="917f1-117">Determines whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="917f1-118">Alcuni file non supportano la ricerca.</span><span class="sxs-lookup"><span data-stu-id="917f1-118">Some files do not support seeking.</span></span>                                                       |
| <span data-ttu-id="917f1-119">fastForward</span><span class="sxs-lookup"><span data-stu-id="917f1-119">fastForward</span></span>     | <span data-ttu-id="917f1-120">Determina se il file supporta l'avanzamento rapido e se tale funzionalità può essere richiamata.</span><span class="sxs-lookup"><span data-stu-id="917f1-120">Determines whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="917f1-121">Molti tipi di file (o flussi live) non supportano fastForward.</span><span class="sxs-lookup"><span data-stu-id="917f1-121">Many file types (or live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="917f1-122">fastReverse</span><span class="sxs-lookup"><span data-stu-id="917f1-122">fastReverse</span></span>     | <span data-ttu-id="917f1-123">Determina se il file supporta fastReverse e se tale funzionalità può essere richiamata.</span><span class="sxs-lookup"><span data-stu-id="917f1-123">Determines whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="917f1-124">Molti tipi di file (o flussi live) non supportano fastReverse.</span><span class="sxs-lookup"><span data-stu-id="917f1-124">Many file types (or live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="917f1-125">Avanti</span><span class="sxs-lookup"><span data-stu-id="917f1-125">next</span></span>            | <span data-ttu-id="917f1-126">Determina se l'utente può cercare la voce successiva in una playlist.</span><span class="sxs-lookup"><span data-stu-id="917f1-126">Determines whether the user can seek to the next entry in a playlist.</span></span>                                                                                             |
| <span data-ttu-id="917f1-127">Sospendi</span><span class="sxs-lookup"><span data-stu-id="917f1-127">pause</span></span>           | <span data-ttu-id="917f1-128">Determina se il metodo **pause** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="917f1-128">Determines whether the **pause** method is available.</span></span>                                                                                                             |
| <span data-ttu-id="917f1-129">Play</span><span class="sxs-lookup"><span data-stu-id="917f1-129">play</span></span>            | <span data-ttu-id="917f1-130">Determina se il metodo **Play** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="917f1-130">Determines whether the **play** method is available.</span></span>                                                                                                              |
| <span data-ttu-id="917f1-131">previous</span><span class="sxs-lookup"><span data-stu-id="917f1-131">previous</span></span>        | <span data-ttu-id="917f1-132">Determina se l'utente può cercare la voce precedente in una playlist.</span><span class="sxs-lookup"><span data-stu-id="917f1-132">Determines whether the user can seek to the previous entry in a playlist.</span></span>                                                                                         |
| <span data-ttu-id="917f1-133">step</span><span class="sxs-lookup"><span data-stu-id="917f1-133">step</span></span>            | <span data-ttu-id="917f1-134">Determina se il metodo **Step** è disponibile durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="917f1-134">Determines whether the **step** method is available during playback.</span></span>                                                                                              |
| <span data-ttu-id="917f1-135">stop</span><span class="sxs-lookup"><span data-stu-id="917f1-135">stop</span></span>            | <span data-ttu-id="917f1-136">Determina se il metodo **Stop** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="917f1-136">Determines whether the **stop** method is available.</span></span>                                                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="917f1-137">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="917f1-137">Return Values</span></span>

<span data-ttu-id="917f1-138">Questo metodo restituisce un valore **booleano** .</span><span class="sxs-lookup"><span data-stu-id="917f1-138">This method returns a **Boolean** value.</span></span>

## <a name="examples"></a><span data-ttu-id="917f1-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="917f1-139">Examples</span></span>

<span data-ttu-id="917f1-140">Nell'esempio seguente viene creato un elemento BUTTON HTML che cerca la posizione iniziale dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="917f1-140">The following example creates an HTML BUTTON element that seeks to the starting position of the current media item.</span></span> <span data-ttu-id="917f1-141">Il codice **JScript utilizza l'** oggetto per verificare che il file supporti l'operazione Seek.</span><span class="sxs-lookup"><span data-stu-id="917f1-141">The JScript code uses **isAvailable** to verify that the file supports the seek operation.</span></span> <span data-ttu-id="917f1-142">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="917f1-142">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a><span data-ttu-id="917f1-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="917f1-143">Requirements</span></span>



| <span data-ttu-id="917f1-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="917f1-144">Requirement</span></span> | <span data-ttu-id="917f1-145">Valore</span><span class="sxs-lookup"><span data-stu-id="917f1-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="917f1-146">Versione</span><span class="sxs-lookup"><span data-stu-id="917f1-146">Version</span></span><br/> | <span data-ttu-id="917f1-147">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="917f1-147">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="917f1-148">DLL</span><span class="sxs-lookup"><span data-stu-id="917f1-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="917f1-149"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="917f1-149"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="917f1-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="917f1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917f1-151">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="917f1-151">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





