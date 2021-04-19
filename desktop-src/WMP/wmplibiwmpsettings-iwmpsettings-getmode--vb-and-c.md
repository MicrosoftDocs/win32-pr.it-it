---
title: Metodo GetMode IWMPSettings
description: Il metodo GetMode restituisce un valore che indica se la modalità ciclo o shuffle è attiva.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- Metodo GetMode Windows Media Player
- Metodo GetMode Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, metodo GetMode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327480"
---
# <a name="iwmpsettingsgetmode-method"></a><span data-ttu-id="099bd-106">Metodo IWMPSettings:: GetMode</span><span class="sxs-lookup"><span data-stu-id="099bd-106">IWMPSettings::getMode method</span></span>

<span data-ttu-id="099bd-107">Il metodo **GetMode** restituisce un valore che indica se la modalità ciclo o shuffle è attiva.</span><span class="sxs-lookup"><span data-stu-id="099bd-107">The **getMode** method returns a value indicating whether loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="099bd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="099bd-108">Syntax</span></span>


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a><span data-ttu-id="099bd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="099bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099bd-110">*bstrMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="099bd-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="099bd-111">**System. String** che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="099bd-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="099bd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="099bd-112">Value</span></span>      | <span data-ttu-id="099bd-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="099bd-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="099bd-114">riavvolgimento rapido</span><span class="sxs-lookup"><span data-stu-id="099bd-114">autoRewind</span></span> | <span data-ttu-id="099bd-115">Le tracce vengono riavviate dall'inizio dopo la riproduzione fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="099bd-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="099bd-116">loop</span><span class="sxs-lookup"><span data-stu-id="099bd-116">loop</span></span>       | <span data-ttu-id="099bd-117">La sequenza di tracce si ripete.</span><span class="sxs-lookup"><span data-stu-id="099bd-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="099bd-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="099bd-118">showFrame</span></span>  | <span data-ttu-id="099bd-119">Il fotogramma chiave più vicino viene visualizzato in caso di mancata riproduzione.</span><span class="sxs-lookup"><span data-stu-id="099bd-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="099bd-120">Questa modalità non è pertinente per le tracce audio.</span><span class="sxs-lookup"><span data-stu-id="099bd-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="099bd-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="099bd-121">shuffle</span></span>    | <span data-ttu-id="099bd-122">Le tracce vengono riprodotte in ordine casuale.</span><span class="sxs-lookup"><span data-stu-id="099bd-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099bd-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="099bd-123">Return value</span></span>

<span data-ttu-id="099bd-124">Valore **System. Boolean** che indica se la modalità specificata è attiva.</span><span class="sxs-lookup"><span data-stu-id="099bd-124">A **System.Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="099bd-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="099bd-125">Requirements</span></span>



| <span data-ttu-id="099bd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="099bd-126">Requirement</span></span> | <span data-ttu-id="099bd-127">Valore</span><span class="sxs-lookup"><span data-stu-id="099bd-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="099bd-128">Versione</span><span class="sxs-lookup"><span data-stu-id="099bd-128">Version</span></span><br/>   | <span data-ttu-id="099bd-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="099bd-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="099bd-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="099bd-130">Namespace</span></span><br/> | <span data-ttu-id="099bd-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="099bd-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="099bd-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="099bd-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="099bd-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="099bd-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099bd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="099bd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099bd-135">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="099bd-135">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="099bd-136">**IWMPSettings. semode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="099bd-136">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





