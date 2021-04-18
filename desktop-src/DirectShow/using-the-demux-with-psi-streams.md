---
description: Uso di Demux con flussi PSI
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Uso di Demux con flussi PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314394"
---
# <a name="using-the-demux-with-psi-streams"></a>Uso di Demux con flussi PSI

Per ottenere informazioni PSI da un flusso di trasporto MPEG-2 usando il filtro MPEG-2 demux, creare un pin di output in Demux con il seguente tipo di supporto:

-   Tipo principale: KSDATAFORMAT di \_ tipo \_ MPEG2 \_ sezioni
-   Sottotipo: MEDIASUBTYPE \_ None
-   Tipo di formato: GUID \_ null

Chiamare quindi il metodo [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) del PIN di output con il PID desiderato e il flag media \_ MPEG2 \_ psi.


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



Ogni sezione complete PSI viene fornita in un esempio di supporto. Per recuperare il numero PID associato a una sezione della tabella, chiamare [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio multimediale. Il PID viene fornito nei 13 bit meno significativi del flag **dwTypeSpecificFlags** nella struttura delle **\_ \_ Proprietà SAMPLE2** . Questa opzione è utile se si esegue il mapping di più PID PSI allo stesso pin di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



