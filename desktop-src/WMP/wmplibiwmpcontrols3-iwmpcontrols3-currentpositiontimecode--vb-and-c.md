---
title: Proprietà currentPositionTimecode di IWMPControls3
description: La proprietà currentPositionTimecode Ottiene o imposta la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale. Questa proprietà attualmente supporta il codice ora SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Finestra delle proprietà di currentPositionTimecode Media Player
- Proprietà di currentPositionTimecode Media Player Windows, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, proprietà currentPositionTimecode
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332456"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a><span data-ttu-id="40f98-107">Proprietà IWMPControls3:: currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="40f98-107">IWMPControls3::currentPositionTimecode property</span></span>

<span data-ttu-id="40f98-108">La proprietà **currentPositionTimecode** Ottiene o imposta la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale.</span><span class="sxs-lookup"><span data-stu-id="40f98-108">The **currentPositionTimecode** property gets or sets the current position in the current media item using a time code format.</span></span> <span data-ttu-id="40f98-109">Questa proprietà attualmente supporta il codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="40f98-109">This property currently supports SMPTE time code.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f98-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40f98-110">Syntax</span></span>


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a><span data-ttu-id="40f98-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="40f98-111">Property value</span></span>

<span data-ttu-id="40f98-112">**System. String** che rappresenta il codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="40f98-112">A **System.String** that is the SMPTE time code.</span></span>

## <a name="remarks"></a><span data-ttu-id="40f98-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="40f98-113">Remarks</span></span>

<span data-ttu-id="40f98-114">Il codice di ora SMPTE fornisce un modo standard per identificare un singolo frame video, utile per sincronizzare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="40f98-114">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="40f98-115">Se un file multimediale digitale supporta il codice ora SMPTE, Windows Media Player possibile recuperare le informazioni sulla posizione del codice ora corrente o cercare un frame video identificato da un particolare codice temporale.</span><span class="sxs-lookup"><span data-stu-id="40f98-115">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code.</span></span>

<span data-ttu-id="40f98-116">Il codice di ora SMPTE identifica un frame specifico per il numero di ore, minuti, secondi e frame che lo separa da un particolare frame di riferimento il frame designato come ora zero.</span><span class="sxs-lookup"><span data-stu-id="40f98-116">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="40f98-117">In genere, il fotogramma ora zero è l'inizio del file e un determinato valore del codice ora SMPTE rappresenta il tempo trascorso dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="40f98-117">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="40f98-118">Il codice temporale è nell'intervallo di formato \[  \] *HH*:*mm*:*SS*.*FF* con \[ *intervallo* \] che rappresenta l'intervallo, hh rappresenta le ore, *mm* rappresenta minuti, *SS* rappresenta i secondi e *FF* rappresenta i frame.</span><span class="sxs-lookup"><span data-stu-id="40f98-118">The time code is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, hh represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="40f98-119">Quando si imposta un valore per **currentPositionTimecode**, è necessario includere tutte e otto le cifre, usando zeri come segnaposto.</span><span class="sxs-lookup"><span data-stu-id="40f98-119">When setting a value for **currentPositionTimecode**, you must include all eight digits, using zeros as placeholders.</span></span>

<span data-ttu-id="40f98-120">\[*intervallo* \] corrisponde al membro **Wrange** della struttura di **dati dell'estensione del \_ timecode \_ \_ WMT** del formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="40f98-120">\[*range*\] corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="40f98-121">Per ulteriori informazioni sugli intervalli di codice temporali, vedere Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="40f98-121">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="40f98-122">L'impostazione e il recupero di **currentPositionTimecode** sono supportati solo per i file che contengono informazioni sul codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="40f98-122">Setting and getting **currentPositionTimecode** is supported only for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="40f98-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="40f98-123">Examples</span></span>

<span data-ttu-id="40f98-124">Nell'esempio di codice seguente viene specificato **currentPositionTimecode** come 1 ora, zero minuti, 30 secondi e 5 fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="40f98-124">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="40f98-125">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="40f98-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a><span data-ttu-id="40f98-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40f98-126">Requirements</span></span>



| <span data-ttu-id="40f98-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f98-127">Requirement</span></span> | <span data-ttu-id="40f98-128">Valore</span><span class="sxs-lookup"><span data-stu-id="40f98-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f98-129">Versione</span><span class="sxs-lookup"><span data-stu-id="40f98-129">Version</span></span><br/>   | <span data-ttu-id="40f98-130">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="40f98-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="40f98-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="40f98-131">Namespace</span></span><br/> | <span data-ttu-id="40f98-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="40f98-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="40f98-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="40f98-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="40f98-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="40f98-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f98-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40f98-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f98-136">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="40f98-136">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





