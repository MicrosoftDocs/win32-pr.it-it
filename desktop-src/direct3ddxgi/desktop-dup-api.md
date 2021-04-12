---
description: Windows 8 Disabilita i driver mirror standard di Windows 2000 Display Driver Model (XDDM) e offre invece l'API per la duplicazione dei desktop.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API di duplicazione desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481077"
---
# <a name="desktop-duplication-api"></a>API di duplicazione desktop

Windows 8 Disabilita i driver mirror standard di Windows 2000 Display Driver Model (XDDM) e offre invece l'API per la duplicazione dei desktop. L'API di duplicazione desktop fornisce accesso remoto a un'immagine desktop per scenari di collaborazione. Le app possono usare l'API di duplicazione desktop per accedere agli aggiornamenti frame per fotogramma sul desktop. Poiché le app ricevono aggiornamenti per l'immagine desktop in una superficie DXGI, le app possono sfruttare tutte le potenzialità della GPU per elaborare gli aggiornamenti delle immagini.

-   [Aggiornamento dei dati dell'immagine desktop](#updating-the-desktop-image-data)
-   [Rotazione dell'immagine desktop](#rotating-the-desktop-image)
-   [Aggiornamento del puntatore del desktop](#updating-the-desktop-pointer)
-   [Argomenti correlati](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Aggiornamento dei dati dell'immagine desktop

DXGI fornisce una superficie che contiene un'immagine desktop corrente tramite il nuovo metodo [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) . Il formato dell'immagine desktop è sempre [**DXGI \_ formato \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , indipendentemente dalla modalità di visualizzazione corrente. Insieme a questa superficie, questi metodi [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) restituiscono i tipi di informazioni indicati che consentono di determinare i pixel all'interno della superficie che è necessario elaborare:

-   [**IDXGIOutputDuplication:: GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) restituisce aree dirty, ovvero rettangoli non sovrapposti che indicano le aree dell'immagine desktop aggiornate dal sistema operativo dopo l'elaborazione dell'immagine desktop precedente.
-   [**IDXGIOutputDuplication:: GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) restituisce le aree di spostamento, che sono rettangoli di pixel nell'immagine desktop che il sistema operativo ha spostato in un'altra posizione all'interno della stessa immagine. Ogni area di spostamento è costituita da un rettangolo di destinazione e da un punto di origine. Il punto di origine specifica il percorso da cui il sistema operativo ha copiato l'area e il rettangolo di destinazione specifica dove il sistema operativo ha spostato tale area. Le aree di spostamento sono sempre aree non estese, pertanto l'origine ha sempre le stesse dimensioni della destinazione.

Si supponga che l'immagine desktop sia stata trasmessa su una connessione lenta all'app client remota. La quantità di dati inviati sulla connessione viene ridotta ricevendo solo i dati sul modo in cui l'app client deve spostare le aree di pixel anziché i dati effettivi sui pixel. Per elaborare lo spostamento, l'app client deve avere archiviato l'ultima immagine completa.

Sebbene il sistema operativo accumuli aggiornamenti di immagini desktop non elaborati, lo spazio potrebbe esaurirsi per archiviare accuratamente le aree di aggiornamento. In questa situazione, il sistema operativo inizia ad accumulare gli aggiornamenti unendoli con le aree di aggiornamento esistenti per coprire tutti i nuovi aggiornamenti. Di conseguenza, il sistema operativo copre i pixel che non sono ancora stati aggiornati in quel frame. Questa situazione, tuttavia, non genera problemi visivi nell'app client perché si riceve l'intera immagine desktop e non solo i pixel aggiornati.

Per ricostruire l'immagine desktop corretta, l'app client deve prima elaborare tutte le aree di spostamento e quindi elaborare tutte le aree dirty. Uno di questi elenchi di aree dirty e di spostamento può essere completamente vuoto. Il codice di esempio dell' [esempio di duplicazione dei desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) Mostra come elaborare le aree dirty e Move in un singolo frame:


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



## <a name="rotating-the-desktop-image"></a>Rotazione dell'immagine desktop

È necessario aggiungere codice esplicito all'app client di duplicazione desktop per supportare le modalità ruotate. In una modalità ruotata la superficie ricevuta da [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) è sempre nell'orientamento non ruotato e l'immagine desktop viene ruotata all'interno della superficie. Se, ad esempio, il desktop è impostato su 768x1024 a 90 gradi di rotazione, **AcquireNextFrame** restituisce una superficie 1024x768 con l'immagine del desktop ruotata al suo interno. Di seguito sono riportati alcuni esempi di rotazione.



| Modalità di visualizzazione impostata dal pannello di controllo di visualizzazione | Modalità di visualizzazione restituita da GDI o DXGI | Superficie restituita da [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| orizzontale 1024x768                          | rotazione di 1024x768 0 gradi           | \[nuova riga 1024x768\] ![Desktop remoto non ruotato](images/dxgi-outdupl-0-rotate.png)<br/>            |
| verticale 1024x768                           | rotazione 768x1024 90 Degree          | \[nuova riga 1024x768\] ![Desktop remoto ruotato di 90 gradi](images/dxgi-outdupl-90-rotate.png)<br/>   |
| orizzontale 1024x768 (capovolto)                | rotazione di 180 gradi 1024x768         | \[nuova riga 1024x768\] ![Desktop remoto ruotato di 180 gradi](images/dxgi-outdupl-180-rotate.png)<br/> |
| verticale da 1024x768 (capovolto)                 | rotazione 768x1024 270 degree         | \[nuova riga 1024x768\] ![Desktop remoto ruotato di 270 gradi](images/dxgi-outdupl-270-rotate.png)<br/> |



 

Il codice nell'app client di duplicazione desktop deve ruotare l'immagine desktop in modo appropriato prima di visualizzare l'immagine del desktop.

> [!Note]  
> Negli scenari con più monitor è possibile ruotare l'immagine del desktop per ogni monitoraggio in modo indipendente.

 

## <a name="updating-the-desktop-pointer"></a>Aggiornamento del puntatore del desktop

È necessario usare l'API di duplicazione desktop per determinare se l'app client deve disegnare la forma puntatore del mouse sull'immagine desktop. Il puntatore del mouse è già disegnato nell'immagine desktop fornita da [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) oppure il puntatore del mouse è separato dall'immagine desktop. Se il puntatore del mouse viene disegnato sull'immagine desktop, i dati di posizione del puntatore segnalati da **AcquireNextFrame** (nel membro **PointerPosition** di [**DXGI \_ OUTDUPL \_ frame \_ info**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) a cui punta il parametro *pFrameInfo* ) indicano che un puntatore separato non è visibile. Se la scheda grafica sovrappone il puntatore del mouse sulla parte superiore dell'immagine del desktop, **AcquireNextFrame** segnala che è visibile un puntatore separato. Quindi, l'app client deve disegnare la forma puntatore del mouse sull'immagine desktop per rappresentare in modo accurato ciò che l'utente corrente vedrà sul monitoraggio.

Per creare il puntatore del mouse sul desktop, usare il membro **PointerPosition** di [**DXGI \_ OUTDUPL \_ frame \_ info**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) dal parametro *pFrameInfo* di [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) per determinare la posizione in cui posizionare l'angolo superiore sinistro del puntatore del mouse sull'immagine desktop. Quando si crea il primo frame, è necessario usare il metodo [**IDXGIOutputDuplication:: GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) per ottenere informazioni sulla forma del puntatore del mouse. Ogni chiamata a **AcquireNextFrame** per ottenere il frame successivo fornisce anche la posizione corrente del puntatore per quel frame. D'altra parte, è necessario usare nuovamente **GetFramePointerShape** solo se la forma viene modificata. Quindi, conserva una copia dell'ultima immagine puntatore e la usa per disegnare sul desktop, a meno che la forma del puntatore del mouse non venga modificata.

> [!Note]  
> Insieme all'immagine della forma puntatore, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) fornisce le dimensioni della posizione sensibile. L'area sensibile viene fornita solo a scopo informativo. La posizione in cui creare l'immagine del puntatore è indipendente dall'area sensibile.

 

Questo esempio di codice dell' [esempio di duplicazione dei desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) Mostra come ottenere la forma del puntatore del mouse:


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

[Miglioramenti di DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
