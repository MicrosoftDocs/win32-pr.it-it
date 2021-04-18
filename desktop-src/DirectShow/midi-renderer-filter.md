---
description: Il filtro renderer MIDI esegue il rendering dei dati MIDI dal filtro del parser MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro renderer MIDI (Windows. Devices. MIDI. h)
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
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331434"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="77f32-103">Filtro renderer MIDI</span><span class="sxs-lookup"><span data-stu-id="77f32-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="77f32-104">Il filtro renderer MIDI esegue il rendering dei dati MIDI dal filtro del [parser MIDI](midi-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="77f32-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f32-105">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="77f32-105">Filter Interfaces</span></span>                        | <span data-ttu-id="77f32-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="77f32-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="77f32-107">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="77f32-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="77f32-108">MEDIATYPE \_ MIDI, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="77f32-108">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="77f32-109">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="77f32-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="77f32-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="77f32-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="77f32-111">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="77f32-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="77f32-112">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="77f32-112">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="77f32-113">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="77f32-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="77f32-114">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="77f32-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="77f32-115">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="77f32-115">Filter CLSID</span></span>                             | <span data-ttu-id="77f32-116">\_AVIMIDIRENDER CLSID</span><span class="sxs-lookup"><span data-stu-id="77f32-116">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="77f32-117">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="77f32-117">Property Page CLSID</span></span>                      | <span data-ttu-id="77f32-118">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="77f32-118">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="77f32-119">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="77f32-119">Executable</span></span>                               | <span data-ttu-id="77f32-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="77f32-120">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="77f32-121">Merito</span><span class="sxs-lookup"><span data-stu-id="77f32-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="77f32-122">\_preferenza preferita</span><span class="sxs-lookup"><span data-stu-id="77f32-122">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="77f32-123">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="77f32-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="77f32-124">\_MIDIRENDERERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="77f32-124">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="77f32-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="77f32-125">Remarks</span></span>

<span data-ttu-id="77f32-126">Il GUID per il tipo di formato è **null**, ma il blocco di formato contiene la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="77f32-126">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="77f32-127">Il membro **dwDivision** specifica la divisione dell'ora del file.</span><span class="sxs-lookup"><span data-stu-id="77f32-127">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="77f32-128">La divisione temporale viene specificata nell'intestazione di qualsiasi file MIDI standard (SMF), nel `MThd` blocco.</span><span class="sxs-lookup"><span data-stu-id="77f32-128">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="77f32-129">Il renderer MIDI imposta questa proprietà sul flusso di dati MIDI chiamando la funzione **midiStreamProperty** .</span><span class="sxs-lookup"><span data-stu-id="77f32-129">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="77f32-130">Gli esempi del filtro del parser MIDI contengono un secondo di dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="77f32-130">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="77f32-131">Il renderer MIDI usa la funzione **midiStreamOut** per eseguire il rendering dei dati MIDI.</span><span class="sxs-lookup"><span data-stu-id="77f32-131">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="77f32-132">Ogni esempio è un punto di sincronizzazione: l'inizio del buffer contiene tutti i comandi necessari per impostare lo stato corretto per il rendering del buffer.</span><span class="sxs-lookup"><span data-stu-id="77f32-132">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="77f32-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77f32-133">Requirements</span></span>



| <span data-ttu-id="77f32-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f32-134">Requirement</span></span> | <span data-ttu-id="77f32-135">Valore</span><span class="sxs-lookup"><span data-stu-id="77f32-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f32-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77f32-136">Header</span></span><br/> | <dl> <span data-ttu-id="77f32-137"><dt>Windows. Devices. MIDI. h</dt></span><span class="sxs-lookup"><span data-stu-id="77f32-137"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f32-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77f32-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f32-139">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="77f32-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




