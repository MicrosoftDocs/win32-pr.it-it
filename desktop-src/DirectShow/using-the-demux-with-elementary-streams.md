---
description: Uso di Demux con flussi elementari
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Uso di Demux con flussi elementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346396"
---
# <a name="using-the-demux-with-elementary-streams"></a>Uso di Demux con flussi elementari

Quando il demux MPEG-2 fornisce payload di PES, invia il flusso di byte ES in batch di esempi di supporti. La dimensione predefinita del campione è 8 KB. Il demux avvia un nuovo esempio di supporto in ogni limite PES, ma può suddividere un singolo payload di PES in diversi esempi. Se, ad esempio, un payload PES è 20.000, verrà distribuito in due campioni da 8 KB seguiti da un campione 4K. Demux non esamina il contenuto del flusso di byte. Il decodificatore analizza le intestazioni di sequenza e cerca le modifiche del formato.

Quando il pin di output del filtro demux si connette al decodificatore, offre il tipo di supporto che è stato specificato al momento della creazione del PIN. Poiché demux non esamina il flusso di byte ES, non convalida il tipo di supporto. In teoria, un decodificatore MPEG-2 dovrebbe essere in grado di connettersi solo con il tipo e il sottotipo principale, per indicare il tipo di dati. Il decodificatore deve quindi esaminare le intestazioni di sequenza che arrivano negli esempi di supporti. Tuttavia, in pratica, molti decodificatori non si connetteranno, a meno che il tipo di supporto non includa un blocco di formato completo.

Si supponga, ad esempio, che PID 0x31 contenga il video del profilo principale MPEG-2. Come minimo, è necessario eseguire i passaggi seguenti.

Per prima cosa, creare un tipo di supporto per il video MPEG-2. A questo punto, lasciare il blocco di formato:


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



Successivamente, creare un pin di output in Demux:


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



Eseguire quindi una query sul nuovo PIN per l'interfaccia **IMPEG2PIDMap** e chiamare **MapPID**. Specificare il numero PID 0x30 e il \_ flusso elementare multimediale \_ per i payload PES.


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



Infine, rilasciare tutte le interfacce al termine dell'operazione:


```C++
pPin0->Release();
pDemux->Release();
```



Di seguito è riportato un esempio più completo di impostazione del tipo di supporto, incluso il blocco di formato. In questo esempio si presuppone ancora un video del profilo principale MPEG-2. I dettagli variano a seconda del contenuto del flusso:


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



