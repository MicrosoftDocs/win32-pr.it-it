---
description: 'Creazione di una sequenza temporale: codice di esempio'
ms.assetid: efe6e8d7-2465-4374-8c99-a410091f8d46
title: 'Creazione di una sequenza temporale: codice di esempio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877bd79b055171dfa5bd12cff0ae257d60e76a16
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304323"
---
# <a name="creating-a-timeline-example-code"></a>Creazione di una sequenza temporale: codice di esempio

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Nell'esempio di codice seguente viene illustrato come creare e visualizzare in anteprima una sequenza temporale nei [servizi di modifica DirectShow](directshow-editing-services.md).

> [!Note]  
> Per motivi di brevità, il codice di esempio non esegue alcun controllo degli errori. In un'applicazione reale, è consigliabile controllare i valori restituiti delle chiamate al metodo per assicurarsi che nessuno abbia avuto esito negativo.

 


```C++
#include <dshow.h>
#include <qedit.h>

// Preview a timeline.
void PreviewTL(IAMTimeline *pTL, IRenderEngine *pRender) 
{
    IGraphBuilder   *pGraph = NULL;
    IMediaControl   *pControl = NULL;
    IMediaEvent     *pEvent = NULL;

    // Build the graph.
    pRender->SetTimelineObject(pTL);
    pRender->ConnectFrontEnd( );
    pRender->RenderOutputPins( );

    // Run the graph.
    pRender->GetFilterGraph(&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
    pControl->Run();

    long evCode;
    pEvent->WaitForCompletion(INFINITE, &evCode);
    pControl->Stop();

    // Clean up.
    pEvent->Release();
    pControl->Release();
    pGraph->Release();
}

void main( void )
{
    // Start by making an empty timeline.

    IAMTimeline    *pTL = NULL;
    CoInitialize(NULL);
    CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);

    // GROUP: Add a video group to the timeline. 

    IAMTimelineGroup    *pGroup = NULL;
    IAMTimelineObj      *pGroupObj = NULL;
    pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
    pGroupObj->QueryInterface(IID_IAMTimelineGroup, (void **)&pGroup);

    // Set the group media type. This example sets the type to "video" and
    // lets DES pick the default settings. For a more detailed example,
    // see "Setting the Group Media Type."
    AM_MEDIA_TYPE mtGroup;  
    ZeroMemory(&mtGroup, sizeof(AM_MEDIA_TYPE));
    mtGroup.majortype = MEDIATYPE_Video;
    pGroup->SetMediaType(&mtGroup);
    pTL->AddGroup(pGroupObj);
    pGroupObj->Release();

    // TRACK: Add a track to the group. 

    IAMTimelineObj      *pTrackObj;
    IAMTimelineTrack    *pTrack;
    IAMTimelineComp     *pComp = NULL;

    pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
    pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
    pComp->VTrackInsBefore(pTrackObj, 0);
    pTrackObj->QueryInterface(IID_IAMTimelineTrack, (void **)&pTrack);

    pTrackObj->Release();
    pComp->Release();    
    pGroup->Release();

    // SOURCE: Add a source to the track.

    IAMTimelineSrc *pSource = NULL;
    IAMTimelineObj *pSourceObj;
    pTL->CreateEmptyNode(&pSourceObj, TIMELINE_MAJOR_TYPE_SOURCE);
    pSourceObj->QueryInterface(IID_IAMTimelineSrc, (void **)&pSource);

    // Set the times and the file name.
    pSourceObj->SetStartStop(0, 50000000);
    BSTR bstrFile = SysAllocString(OLESTR("C:\\example.avi"));
    pSource->SetMediaName(bstrFile); 
    SysFreeString(bstrFile);
    pSource->SetMediaTimes(40000000, 140000000);
    pTrack->SrcAdd(pSourceObj);

    pSourceObj->Release();
    pSource->Release();
    pTrack->Release();

    // Preview the timeline.
    IRenderEngine *pRenderEngine = NULL;
    CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
        IID_IRenderEngine, (void**) &pRenderEngine);
    PreviewTL(pTL, pRenderEngine);

    // Clean up.
    pRenderEngine->ScrapIt();
    pRenderEngine->Release();
    pTL->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 



