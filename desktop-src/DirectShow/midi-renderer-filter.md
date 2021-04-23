---
description: Il filtro renderer MIDI esegue il rendering dei dati MIDI dal filtro parser MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro renderer MIDI (Windows.devices.midi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909409"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="ea81b-103">Filtro renderer MIDI</span><span class="sxs-lookup"><span data-stu-id="ea81b-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="ea81b-104">Il filtro renderer MIDI esegue il rendering dei dati MIDI dal filtro [parser MIDI.](midi-parser-filter.md)</span><span class="sxs-lookup"><span data-stu-id="ea81b-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



| <span data-ttu-id="ea81b-105">Label</span><span class="sxs-lookup"><span data-stu-id="ea81b-105">Label</span></span> | <span data-ttu-id="ea81b-106">Valore</span><span class="sxs-lookup"><span data-stu-id="ea81b-106">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea81b-107">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="ea81b-107">Filter Interfaces</span></span>                        | <span data-ttu-id="ea81b-108">[**IAMClockSlave,**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave) [**IAMDirectSound,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) [**IAMResourceControl,**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IBasicAudio,**](/windows/desktop/api/Control/nn-control-ibasicaudio) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="ea81b-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="ea81b-109">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="ea81b-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="ea81b-110">MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="ea81b-110">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ea81b-111">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="ea81b-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="ea81b-112">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ea81b-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ea81b-113">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="ea81b-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="ea81b-114">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="ea81b-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ea81b-115">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="ea81b-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="ea81b-116">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="ea81b-116">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ea81b-117">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="ea81b-117">Filter CLSID</span></span>                             | <span data-ttu-id="ea81b-118">CLSID \_ AVIMIDIRender</span><span class="sxs-lookup"><span data-stu-id="ea81b-118">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ea81b-119">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="ea81b-119">Property Page CLSID</span></span>                      | <span data-ttu-id="ea81b-120">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="ea81b-120">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ea81b-121">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="ea81b-121">Executable</span></span>                               | <span data-ttu-id="ea81b-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="ea81b-122">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="ea81b-123">Merito</span><span class="sxs-lookup"><span data-stu-id="ea81b-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="ea81b-124">MERITO \_ PREFERITO</span><span class="sxs-lookup"><span data-stu-id="ea81b-124">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="ea81b-125">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="ea81b-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ea81b-126">CLSID \_ MidiRendererCategory</span><span class="sxs-lookup"><span data-stu-id="ea81b-126">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="ea81b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea81b-127">Remarks</span></span>

<span data-ttu-id="ea81b-128">Il GUID per il tipo di formato è **NULL,** ma il blocco di formato contiene la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="ea81b-128">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="ea81b-129">Il **membro dwDivision** specifica la divisione temporale del file.</span><span class="sxs-lookup"><span data-stu-id="ea81b-129">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="ea81b-130">La divisione temporale viene specificata nell'intestazione di qualsiasi file MIDI standard (SMF) nel `MThd` blocco .</span><span class="sxs-lookup"><span data-stu-id="ea81b-130">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="ea81b-131">Il renderer MIDI imposta questa proprietà nel flusso di dati MIDI chiamando la **funzione midiStreamProperty.**</span><span class="sxs-lookup"><span data-stu-id="ea81b-131">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="ea81b-132">Gli esempi del filtro del parser MIDI contengono un secondo di dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="ea81b-132">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="ea81b-133">Il renderer MIDI usa la **funzione midiStreamOut** per eseguire il rendering dei dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="ea81b-133">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="ea81b-134">Ogni esempio è un punto di sincronizzazione: l'inizio del buffer contiene tutti i comandi necessari per impostare lo stato corretto per il rendering del buffer.</span><span class="sxs-lookup"><span data-stu-id="ea81b-134">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea81b-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea81b-135">Requirements</span></span>



| <span data-ttu-id="ea81b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea81b-136">Requirement</span></span> | <span data-ttu-id="ea81b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ea81b-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea81b-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea81b-138">Header</span></span><br/> | <dl> <span data-ttu-id="ea81b-139"><dt>Windows.devices.midi.h</dt></span><span class="sxs-lookup"><span data-stu-id="ea81b-139"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea81b-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea81b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea81b-141">DirectShow Filters</span><span class="sxs-lookup"><span data-stu-id="ea81b-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




