---
title: Metodo Settings. semode
description: Il metodo semode imposta varie modalità su attivo o inattivo.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- Metodo di Media Player di Windows
- Metodo di Media Player Windows, classe Settings
- Classe Settings Media Player Windows, metodo semode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327369"
---
# <a name="settingssetmode-method"></a><span data-ttu-id="073a7-106">Metodo Settings. semode</span><span class="sxs-lookup"><span data-stu-id="073a7-106">Settings.setMode method</span></span>

<span data-ttu-id="073a7-107">Il metodo **semode** imposta varie modalità su attivo o inattivo.</span><span class="sxs-lookup"><span data-stu-id="073a7-107">The **setMode** method sets various modes to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="073a7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="073a7-108">Syntax</span></span>


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a><span data-ttu-id="073a7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="073a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="073a7-110">*modeName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="073a7-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="073a7-111">**Stringa** che specifica il nome della modalità da modificare, contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="073a7-111">**String** specifying the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="073a7-112">string</span><span class="sxs-lookup"><span data-stu-id="073a7-112">String</span></span>     | <span data-ttu-id="073a7-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="073a7-113">Description</span></span>                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="073a7-114">riavvolgimento rapido</span><span class="sxs-lookup"><span data-stu-id="073a7-114">autoRewind</span></span> | <span data-ttu-id="073a7-115">Modalità che indica se le tracce vengono riferite all'inizio dopo la riproduzione fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="073a7-115">Mode indicating whether the tracks are rewound to the beginning after playing to the end.</span></span> <span data-ttu-id="073a7-116">Lo stato predefinito è true.</span><span class="sxs-lookup"><span data-stu-id="073a7-116">Default state is true.</span></span>                                                  |
| <span data-ttu-id="073a7-117">loop</span><span class="sxs-lookup"><span data-stu-id="073a7-117">loop</span></span>       | <span data-ttu-id="073a7-118">Modalità che indica se la sequenza di tracce si ripete.</span><span class="sxs-lookup"><span data-stu-id="073a7-118">Mode indicating whether the sequence of tracks repeats itself.</span></span> <span data-ttu-id="073a7-119">Lo stato predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="073a7-119">Default state is false.</span></span>                                                                            |
| <span data-ttu-id="073a7-120">showFrame</span><span class="sxs-lookup"><span data-stu-id="073a7-120">showFrame</span></span>  | <span data-ttu-id="073a7-121">Modalità che indica se il fotogramma chiave video più vicino viene visualizzato nella posizione corrente quando non viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="073a7-121">Mode indicating whether the nearest video key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="073a7-122">Lo stato predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="073a7-122">Default state is false.</span></span> <span data-ttu-id="073a7-123">Non ha alcun effetto sulle tracce audio.</span><span class="sxs-lookup"><span data-stu-id="073a7-123">Has no effect on audio tracks.</span></span> |
| <span data-ttu-id="073a7-124">shuffle</span><span class="sxs-lookup"><span data-stu-id="073a7-124">shuffle</span></span>    | <span data-ttu-id="073a7-125">Modalità che indica se le tracce vengono riprodotte in ordine casuale.</span><span class="sxs-lookup"><span data-stu-id="073a7-125">Mode indicating whether the tracks are played in random order.</span></span> <span data-ttu-id="073a7-126">Lo stato predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="073a7-126">Default state is false.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="073a7-127">*stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="073a7-127">*state* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="073a7-128">**Valore booleano** che specifica se la nuova modalità specificata è attiva o meno.</span><span class="sxs-lookup"><span data-stu-id="073a7-128">**Boolean** specifying whether the new specified mode is active or not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="073a7-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="073a7-129">Return value</span></span>

<span data-ttu-id="073a7-130">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="073a7-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="073a7-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="073a7-131">Remarks</span></span>

<span data-ttu-id="073a7-132">Quando la modalità showFrame è attiva, il lettore deve accedere al contenuto della traccia per recuperare il frame video.</span><span class="sxs-lookup"><span data-stu-id="073a7-132">When the showFrame mode is active, the Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="073a7-133">A causa delle considerazioni sulla larghezza di banda, usare questa modalità con cautela quando si giocano contenuti non locali.</span><span class="sxs-lookup"><span data-stu-id="073a7-133">Due to bandwidth considerations, use this mode cautiously when playing non-local content.</span></span>

## <a name="requirements"></a><span data-ttu-id="073a7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="073a7-134">Requirements</span></span>



| <span data-ttu-id="073a7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="073a7-135">Requirement</span></span> | <span data-ttu-id="073a7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="073a7-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="073a7-137">Versione</span><span class="sxs-lookup"><span data-stu-id="073a7-137">Version</span></span><br/> | <span data-ttu-id="073a7-138">Per le modalità ciclo e riproduzione casuale, Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="073a7-138">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="073a7-139">Per le modalità AutoRewind e showFrame, Windows Media Player 9 Series o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="073a7-139">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="073a7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="073a7-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="073a7-141"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="073a7-141"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="073a7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="073a7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073a7-143">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="073a7-143">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="073a7-144">**Settings. getMode**</span><span class="sxs-lookup"><span data-stu-id="073a7-144">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> </dl>

 

 





