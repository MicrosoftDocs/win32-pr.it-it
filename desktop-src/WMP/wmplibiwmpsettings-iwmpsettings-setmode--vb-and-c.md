---
title: IWMPSettings metodo semodalità
description: Il metodo semode imposta la modalità ciclo o shuffle su attivo o inattivo.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- Metodo di Media Player di Windows
- Metodo di Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, metodo semode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324520"
---
# <a name="iwmpsettingssetmode-method"></a><span data-ttu-id="99882-106">Metodo IWMPSettings:: toMode</span><span class="sxs-lookup"><span data-stu-id="99882-106">IWMPSettings::setMode method</span></span>

<span data-ttu-id="99882-107">Il metodo **semode** imposta la modalità ciclo o shuffle su attivo o inattivo.</span><span class="sxs-lookup"><span data-stu-id="99882-107">The **setMode** method sets the loop mode or shuffle mode to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="99882-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99882-108">Syntax</span></span>


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a><span data-ttu-id="99882-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="99882-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99882-110">*bstrMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99882-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99882-111">**System. String** che rappresenta il nome della modalità da modificare, contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="99882-111">A **System.String** that is the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="99882-112">Valore</span><span class="sxs-lookup"><span data-stu-id="99882-112">Value</span></span>      | <span data-ttu-id="99882-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99882-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99882-114">riavvolgimento rapido</span><span class="sxs-lookup"><span data-stu-id="99882-114">autoRewind</span></span> | <span data-ttu-id="99882-115">Le tracce vengono riavviate dall'inizio dopo la riproduzione fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="99882-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="99882-116">loop</span><span class="sxs-lookup"><span data-stu-id="99882-116">loop</span></span>       | <span data-ttu-id="99882-117">La sequenza di tracce si ripete.</span><span class="sxs-lookup"><span data-stu-id="99882-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="99882-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="99882-118">showFrame</span></span>  | <span data-ttu-id="99882-119">Il fotogramma chiave più vicino viene visualizzato in caso di mancata riproduzione.</span><span class="sxs-lookup"><span data-stu-id="99882-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="99882-120">Questa modalità non è pertinente per le tracce audio.</span><span class="sxs-lookup"><span data-stu-id="99882-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="99882-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="99882-121">shuffle</span></span>    | <span data-ttu-id="99882-122">Le tracce vengono riprodotte in ordine casuale.</span><span class="sxs-lookup"><span data-stu-id="99882-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> <dt>

<span data-ttu-id="99882-123">*varfMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99882-123">*varfMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99882-124">Valore **System. Boolean** che specifica se la nuova modalità specificata è attiva.</span><span class="sxs-lookup"><span data-stu-id="99882-124">A **System.Boolean** value specifying whether the new specified mode is active.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99882-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99882-125">Return value</span></span>

<span data-ttu-id="99882-126">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="99882-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99882-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="99882-127">Remarks</span></span>

<span data-ttu-id="99882-128">Quando la modalità showFrame è attiva, Windows Media Player deve accedere al contenuto della traccia per recuperare il frame video.</span><span class="sxs-lookup"><span data-stu-id="99882-128">When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="99882-129">Usare questa modalità con cautela per la riproduzione di contenuto non locale.</span><span class="sxs-lookup"><span data-stu-id="99882-129">Use this mode cautiously when playing content that is not local.</span></span>

## <a name="requirements"></a><span data-ttu-id="99882-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99882-130">Requirements</span></span>



| <span data-ttu-id="99882-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="99882-131">Requirement</span></span> | <span data-ttu-id="99882-132">Valore</span><span class="sxs-lookup"><span data-stu-id="99882-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99882-133">Versione</span><span class="sxs-lookup"><span data-stu-id="99882-133">Version</span></span><br/>   | <span data-ttu-id="99882-134">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="99882-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="99882-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="99882-135">Namespace</span></span><br/> | <span data-ttu-id="99882-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="99882-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="99882-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="99882-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="99882-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="99882-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99882-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99882-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99882-140">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="99882-140">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="99882-141">**IWMPSettings. getMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="99882-141">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





