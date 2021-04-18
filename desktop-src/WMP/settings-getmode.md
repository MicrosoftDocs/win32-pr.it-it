---
title: Metodo Settings. getMode
description: Il metodo GetMode determina se la modalità ciclo o shuffle è attiva.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- Metodo GetMode Windows Media Player
- Metodo GetMode Windows Media Player, classe Settings
- Classe Settings Media Player Windows, metodo GetMode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327384"
---
# <a name="settingsgetmode-method"></a><span data-ttu-id="0b71c-106">Metodo Settings. getMode</span><span class="sxs-lookup"><span data-stu-id="0b71c-106">Settings.getMode method</span></span>

<span data-ttu-id="0b71c-107">Il metodo **GetMode** determina se la modalità ciclo o shuffle è attiva.</span><span class="sxs-lookup"><span data-stu-id="0b71c-107">The **getMode** method determines whether the loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b71c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b71c-108">Syntax</span></span>


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a><span data-ttu-id="0b71c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b71c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b71c-110">*modeName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b71c-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b71c-111">**Stringa** che specifica il nome della modalità in questione, contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b71c-111">**String** specifying the name of the mode in question, containing one of the following values.</span></span>



| <span data-ttu-id="0b71c-112">string</span><span class="sxs-lookup"><span data-stu-id="0b71c-112">String</span></span>     | <span data-ttu-id="0b71c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b71c-113">Description</span></span>                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b71c-114">riavvolgimento rapido</span><span class="sxs-lookup"><span data-stu-id="0b71c-114">autoRewind</span></span> | <span data-ttu-id="0b71c-115">Le tracce vengono riavviate all'inizio dopo la riproduzione fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="0b71c-115">Tracks are restarted at the beginning after playing to the end.</span></span>                                                          |
| <span data-ttu-id="0b71c-116">loop</span><span class="sxs-lookup"><span data-stu-id="0b71c-116">loop</span></span>       | <span data-ttu-id="0b71c-117">La sequenza di tracce si ripete.</span><span class="sxs-lookup"><span data-stu-id="0b71c-117">The sequence of tracks repeats itself.</span></span>                                                                                   |
| <span data-ttu-id="0b71c-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="0b71c-118">showFrame</span></span>  | <span data-ttu-id="0b71c-119">Il fotogramma chiave più vicino viene visualizzato nella posizione corrente quando non viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="0b71c-119">The nearest key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="0b71c-120">Questa modalità non è pertinente per le tracce audio.</span><span class="sxs-lookup"><span data-stu-id="0b71c-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="0b71c-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="0b71c-121">shuffle</span></span>    | <span data-ttu-id="0b71c-122">Le tracce vengono riprodotte in ordine casuale.</span><span class="sxs-lookup"><span data-stu-id="0b71c-122">Tracks are played in random order.</span></span>                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b71c-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b71c-123">Return value</span></span>

<span data-ttu-id="0b71c-124">Questo metodo restituisce un valore **booleano** che indica se la modalità specificata è attiva.</span><span class="sxs-lookup"><span data-stu-id="0b71c-124">This method returns a **Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b71c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b71c-125">Requirements</span></span>



| <span data-ttu-id="0b71c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b71c-126">Requirement</span></span> | <span data-ttu-id="0b71c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0b71c-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b71c-128">Versione</span><span class="sxs-lookup"><span data-stu-id="0b71c-128">Version</span></span><br/> | <span data-ttu-id="0b71c-129">Per le modalità ciclo e riproduzione casuale, Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="0b71c-129">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="0b71c-130">Per le modalità AutoRewind e showFrame, Windows Media Player 9 Series o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0b71c-130">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="0b71c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0b71c-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b71c-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b71c-132"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="0b71c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b71c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b71c-134">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="0b71c-134">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="0b71c-135">**Settings. semode**</span><span class="sxs-lookup"><span data-stu-id="0b71c-135">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





