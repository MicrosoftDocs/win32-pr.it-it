---
description: Windows 8 disabilita i driver mirror XDDM (Display Driver Model) standard Windows 2000 e offre invece l'API di duplicazione desktop.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API di duplicazione desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c1960d064d7fd1e34748dcc2efb3c86459b498df91b52c1384ef8698a37c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518497"
---
# <a name="desktop-duplication-api"></a>API di duplicazione desktop

Windows 8 disabilita i driver mirror XDDM (Display Driver Model) standard Windows 2000 e offre invece l'API di duplicazione desktop. L'API di duplicazione desktop fornisce l'accesso remoto a un'immagine desktop per scenari di collaborazione. Le app possono usare l'API di duplicazione desktop per accedere agli aggiornamenti frame per frame al desktop. Poiché le app ricevono aggiornamenti dell'immagine desktop in una superficie DXGI, le app possono usare tutta la potenza della GPU per elaborare gli aggiornamenti dell'immagine.

-   [Aggiornamento dei dati dell'immagine del desktop](#updating-the-desktop-image-data)
-   [Rotazione dell'immagine del desktop](#rotating-the-desktop-image)
-   [Aggiornamento del puntatore del desktop](#updating-the-desktop-pointer)
-   [Argomenti correlati](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Aggiornamento dei dati dell'immagine del desktop

DXGI fornisce una superficie che contiene un'immagine desktop corrente tramite il nuovo [**metodo IDXGIOutputDuplication::AcquireNextFrame.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) Il formato dell'immagine desktop è sempre [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) indipendentemente dalla modalità di visualizzazione corrente. Insieme a questa superficie, questi [**metodi IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) restituiscono i tipi indicati di informazioni che consentono di determinare quali pixel all'interno della superficie è necessario elaborare:

-   [**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) restituisce aree dirty, ovvero rettangoli non sovrapposti che indicano le aree dell'immagine desktop aggiornate dal sistema operativo dopo l'elaborazione dell'immagine desktop precedente.
-   [**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) restituisce aree di spostamento, ovvero rettangoli di pixel nell'immagine desktop spostati dal sistema operativo in un'altra posizione all'interno della stessa immagine. Ogni area di spostamento è costituita da un rettangolo di destinazione e da un punto di origine. Il punto di origine specifica la posizione da cui il sistema operativo ha copiato l'area e il rettangolo di destinazione specifica dove il sistema operativo ha spostato tale area. Le aree di spostamento sono sempre aree non distese, quindi l'origine ha sempre le stesse dimensioni della destinazione.

Si supponga che l'immagine desktop sia stata trasmessa tramite una connessione lenta all'app client remota. La quantità di dati inviati tramite la connessione viene ridotta ricevendo solo i dati sul modo in cui l'app client deve spostare aree di pixel anziché dati pixel effettivi. Per elaborare gli spostamenti, l'app client deve aver archiviato l'ultima immagine completa.

Mentre il sistema operativo accumula gli aggiornamenti delle immagini desktop non elaborate, lo spazio potrebbe essere insufficiente per archiviare in modo accurato le aree di aggiornamento. In questo caso, il sistema operativo inizia ad accumulare gli aggiornamenti unendoli con le aree di aggiornamento esistenti per coprire tutti i nuovi aggiornamenti. Di conseguenza, il sistema operativo copre i pixel non ancora aggiornati in tale frame. Questa situazione, tuttavia, non genera problemi visivi nell'app client perché si riceve l'intera immagine del desktop e non solo i pixel aggiornati.

Per ricostruire l'immagine desktop corretta, l'app client deve prima elaborare tutte le aree di spostamento e quindi elaborare tutte le aree dirty. Uno di questi elenchi di aree dirty e move può essere completamente vuoto. Il codice di esempio dell'esempio [di duplicazione desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) illustra come elaborare le aree dirty e move in un singolo frame:


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a>Rotazione dell'immagine del desktop

È necessario aggiungere codice esplicito all'app client di duplicazione desktop per supportare le modalità ruotate. In modalità ruotata, la superficie ricevuta da [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) è sempre con l'orientamento non ruotato e l'immagine del desktop viene ruotata all'interno della superficie. Ad esempio, se il desktop è impostato su 768x1024 a una rotazione di 90 gradi, **AcquireNextFrame** restituisce una superficie 1024x768 con l'immagine del desktop ruotata al suo interno. Ecco alcuni esempi di rotazione.



| Modalità di visualizzazione impostata dal pannello di controllo dello schermo | Modalità di visualizzazione restituita da GDI o DXGI | Surface restituito da [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| 1024x768 orizzontale                          | Rotazione di 0 gradi 1024x768           | Nuova riga 1024x768 \[\] ![Desktop remoto non torotated](images/dxgi-outdupl-0-rotate.png)<br/>            |
| 1024x768 verticale                           | Rotazione di 768x1024 a 90 gradi          | Nuova riga 1024x768 \[\] ![Desktop remoto ruotato di 90 gradi](images/dxgi-outdupl-90-rotate.png)<br/>   |
| 1024x768 orizzontale (capovolto)                | Rotazione di 1024x768 a 180 gradi         | Nuova riga 1024x768 \[\] ![Desktop remoto ruotato di 180 gradi](images/dxgi-outdupl-180-rotate.png)<br/> |
| 1024x768 verticale (capovolto)                 | Rotazione di 768x1024 a 270 gradi         | Nuova riga 1024x768 \[\] ![Desktop remoto ruotato di 270 gradi](images/dxgi-outdupl-270-rotate.png)<br/> |



 

Il codice nell'app client di duplicazione desktop deve ruotare l'immagine del desktop in modo appropriato prima di visualizzare l'immagine desktop.

> [!Note]  
> Negli scenari con più monitor è possibile ruotare l'immagine del desktop per ogni monitoraggio in modo indipendente.

 

## <a name="updating-the-desktop-pointer"></a>Aggiornamento del puntatore del desktop

È necessario usare l'API di duplicazione del desktop per determinare se l'app client deve disegnare la forma del puntatore del mouse sull'immagine del desktop. Il puntatore del mouse è già disegnato sull'immagine del desktop fornita da [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) oppure il puntatore del mouse è separato dall'immagine del desktop. Se il puntatore del mouse viene disegnato sull'immagine desktop, i dati relativi alla posizione del puntatore segnalati da **AcquireNextFrame** (nel membro **PointerPosition** di [**DXGI \_ OUTDUPL \_ FRAME \_ INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) a cui punta il parametro *pFrameInfo)* indicano che un puntatore separato non è visibile. Se l'adattatore grafico sovrappone il puntatore del mouse sopra l'immagine del desktop, **AcquireNextFrame** segnala che è visibile un puntatore separato. L'app client deve quindi disegnare la forma del puntatore del mouse sull'immagine del desktop per rappresentare in modo accurato ciò che l'utente corrente visualizza sul monitor.

Per disegnare il puntatore del mouse del desktop, usare il membro **PointerPosition** di [**DXGI \_ OUTDUPL \_ FRAME \_ INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) dal *parametro pFrameInfo* di [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) per determinare dove individuare l'angolo superiore sinistro del puntatore del mouse sull'immagine del desktop. Quando si disegna il primo frame, è necessario usare il metodo [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) per ottenere informazioni sulla forma del puntatore del mouse. Ogni chiamata a **AcquireNextFrame** per ottenere il frame successivo fornisce anche la posizione corrente del puntatore per tale frame. D'altra parte, è necessario usare **di nuovo GetFramePointerShape** solo se la forma cambia. Conservare quindi una copia dell'ultima immagine del puntatore e usarla per disegnare sul desktop a meno che la forma del puntatore del mouse non cambi.

> [!Note]  
> Insieme all'immagine della forma del puntatore, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) fornisce le dimensioni della posizione dell'area sensibile. L'area sensibile viene specificata solo a scopo informativo. La posizione in cui disegnare l'immagine del puntatore è indipendente dall'area sensibile.

 

Questo codice di esempio dell'esempio [di duplicazione desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) illustra come ottenere la forma del puntatore del mouse:


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti di DXGI 1.2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
