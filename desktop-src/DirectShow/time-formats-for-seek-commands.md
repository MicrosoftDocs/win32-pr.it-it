---
description: Formati di ora per i comandi seek
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formati di ora per i comandi seek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530325"
---
# <a name="time-formats-for-seek-commands"></a><span data-ttu-id="19a67-103">Formati di ora per i comandi seek</span><span class="sxs-lookup"><span data-stu-id="19a67-103">Time Formats For Seek Commands</span></span>

<span data-ttu-id="19a67-104">Molti dei metodi nell'interfaccia **IMediaSeeking** hanno parametri che esprimono i valori di posizione, ad esempio la posizione corrente o la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="19a67-104">Many of the methods in the **IMediaSeeking** interface have parameters that express position values, such as current position or stop position.</span></span> <span data-ttu-id="19a67-105">Per impostazione predefinita, questi parametri sono espressi in unità di 100 nanosecondi, detti anche ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="19a67-105">By default, these parameters are expressed in units of 100 nanoseconds, also called reference time.</span></span> <span data-ttu-id="19a67-106">Qualsiasi filtro che può essere cercato deve supportare la ricerca in base all'ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="19a67-106">Any filter that can seek must support seeking by reference time.</span></span> <span data-ttu-id="19a67-107">Alcuni filtri possono essere cercati anche usando altre unità di tempo, ad esempio la ricerca di un determinato numero di frame o la ricerca di un offset di byte specificato all'interno di un flusso.</span><span class="sxs-lookup"><span data-stu-id="19a67-107">Some filters can seek using other units of time as well, such as seeking to a particular frame number, or seeking to a given byte offset within a stream.</span></span> <span data-ttu-id="19a67-108">Ognuna di queste unità di tempo è denominata formato ora ed è definita da un identificatore univoco globale (GUID).</span><span class="sxs-lookup"><span data-stu-id="19a67-108">Each of these time units is called a time format, and is defined by a globally unique identifier (GUID).</span></span> <span data-ttu-id="19a67-109">Per un elenco dei formati di ora definiti da DirectShow, vedere GUID del [**formato di ora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="19a67-109">For a list of the time formats that are defined by DirectShow, see [**Time Format GUIDs**](time-format-guids.md).</span></span> <span data-ttu-id="19a67-110">Le terze parti possono anche definire i GUID per i formati di ora personalizzati.</span><span class="sxs-lookup"><span data-stu-id="19a67-110">Third parties can also define GUIDs for custom time formats.</span></span>

<span data-ttu-id="19a67-111">Per determinare se i filtri attualmente presenti nel grafico di filtro supportano un formato di ora specifico, chiamare il metodo [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="19a67-111">To determine whether the filters currently in the filter graph support a particular time format, call the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span> <span data-ttu-id="19a67-112">Il metodo restituisce \_ OK se il formato è supportato.</span><span class="sxs-lookup"><span data-stu-id="19a67-112">The method returns S\_OK if the format is supported.</span></span> <span data-ttu-id="19a67-113">In caso contrario, restituisce \_ false o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="19a67-113">Otherwise, it returns S\_FALSE or an error code.</span></span> <span data-ttu-id="19a67-114">Se un formato è supportato, è possibile passare a tale formato chiamando il metodo [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="19a67-114">If a format is supported, you can switch to that format by calling the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span> <span data-ttu-id="19a67-115">Se il metodo **SetTimeFormat** ha esito positivo, i comandi di ricerca successivi vengono espressi usando il nuovo formato di ora.</span><span class="sxs-lookup"><span data-stu-id="19a67-115">If the **SetTimeFormat** method succeeds, subsequent seek commands are expressed using the new time format.</span></span>

<span data-ttu-id="19a67-116">Nell'esempio seguente viene controllato se il grafo supporta la ricerca in base al numero di frame.</span><span class="sxs-lookup"><span data-stu-id="19a67-116">The follow example checks whether the graph supports seeking by frame number.</span></span> <span data-ttu-id="19a67-117">In caso affermativo, Cerca il frame numero 20:</span><span class="sxs-lookup"><span data-stu-id="19a67-117">If so, it seeks to frame number 20:</span></span>


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



<span data-ttu-id="19a67-118">Si noti che i formati di ora si applicano solo ai comandi Seek.</span><span class="sxs-lookup"><span data-stu-id="19a67-118">Note that time formats only apply to seek commands.</span></span> <span data-ttu-id="19a67-119">Non influiscono sulla riproduzione del grafo o su altre azioni.</span><span class="sxs-lookup"><span data-stu-id="19a67-119">They do not affect graph playback or other actions.</span></span>

 

 



