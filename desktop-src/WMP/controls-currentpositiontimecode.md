---
title: Controls. currentPositionTimecode
description: La proprietà currentPositionTimecode specifica o recupera la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale. Questa proprietà attualmente supporta il codice ora SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Media Player di Windows Controls. currentPositionTimecode
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324831"
---
# <a name="controlscurrentpositiontimecode"></a><span data-ttu-id="3fd01-105">Controls. currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="3fd01-105">Controls.currentPositionTimecode</span></span>

<span data-ttu-id="3fd01-106">La proprietà **currentPositionTimecode** specifica o recupera la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale.</span><span class="sxs-lookup"><span data-stu-id="3fd01-106">The **currentPositionTimecode** property specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="3fd01-107">Questa proprietà attualmente supporta il codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3fd01-107">This property currently supports SMPTE time code.</span></span>

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a><span data-ttu-id="3fd01-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3fd01-108">Possible Values</span></span>

<span data-ttu-id="3fd01-109">Questa proprietà è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3fd01-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd01-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fd01-110">Remarks</span></span>

<span data-ttu-id="3fd01-111">Il codice di ora SMPTE fornisce un modo standard per identificare un singolo frame video, utile per sincronizzare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3fd01-111">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="3fd01-112">Se un file multimediale digitale supporta il codice ora SMPTE, Windows Media Player possibile recuperare le informazioni sulla posizione del codice ora corrente o cercare un frame video identificato da una **stringa** di codice temporale particolare.</span><span class="sxs-lookup"><span data-stu-id="3fd01-112">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code **String**.</span></span>

<span data-ttu-id="3fd01-113">Il codice di ora SMPTE identifica un frame specifico per il numero di ore, minuti, secondi e frame che lo separa da un particolare frame di riferimento il frame designato come ora zero.</span><span class="sxs-lookup"><span data-stu-id="3fd01-113">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="3fd01-114">In genere, il fotogramma ora zero è l'inizio del file e un determinato valore del codice ora SMPTE rappresenta il tempo trascorso dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="3fd01-114">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="3fd01-115">La **stringa** del codice temporale è nell'intervallo di formato \[  \] *HH*:*mm*:*SS*.*FF* con \[ *intervallo* \] che rappresenta l'intervallo, *HH* rappresenta le ore, *mm* rappresenta minuti, *SS* rappresenta i secondi e *FF* rappresenta i frame.</span><span class="sxs-lookup"><span data-stu-id="3fd01-115">The time code **String** is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, *hh* represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="3fd01-116">Quando si specifica un valore usando **currentPositionTimecode**, è necessario includere tutte e otto le cifre usando zeri come segnaposto.</span><span class="sxs-lookup"><span data-stu-id="3fd01-116">When specifying a value using **currentPositionTimecode**, you must include all eight digits using zeros as placeholders.</span></span>

<span data-ttu-id="3fd01-117">L' \[ identificatore di *intervallo* \] corrisponde al membro **Wrange** della struttura di dati dell' **\_ estensione del \_ timecode \_ WMT** del formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3fd01-117">The \[*range*\] specifier corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="3fd01-118">Per ulteriori informazioni sugli intervalli di codice temporali, vedere Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="3fd01-118">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="3fd01-119">La specifica e il recupero di **currentPositionTimecode** sono supportati solo per i file che contengono informazioni sul codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="3fd01-119">Specifying and retrieving **currentPositionTimecode** is only supported for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="3fd01-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="3fd01-120">Examples</span></span>

<span data-ttu-id="3fd01-121">Nell'esempio di codice seguente viene specificato **currentPositionTimecode** come 1 ora, zero minuti, 30 secondi e 5 fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="3fd01-121">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="3fd01-122">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3fd01-122">The **Player** object was created with ID = "Player".</span></span>


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a><span data-ttu-id="3fd01-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fd01-123">Requirements</span></span>



| <span data-ttu-id="3fd01-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd01-124">Requirement</span></span> | <span data-ttu-id="3fd01-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd01-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd01-126">Versione</span><span class="sxs-lookup"><span data-stu-id="3fd01-126">Version</span></span><br/> | <span data-ttu-id="3fd01-127">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="3fd01-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="3fd01-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3fd01-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="3fd01-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fd01-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd01-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fd01-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd01-131">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="3fd01-131">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





