---
description: Uso di Demux con l'Flussi
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Uso di Demux con l'Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec805b4c93432c6532edaefac50e9bd15ad8fac5a7d9672fd358c66e57363fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964671"
---
# <a name="using-the-demux-with-elementary-streams"></a>Uso di Demux con l'Flussi

Quando il demux MPEG-2 recapita payload PES, invia il flusso di byte ES in batch di campioni multimediali. La dimensione predefinita del campione è 8K. Il demux avvia un nuovo campione multimediale in ogni limite PES, ma può suddividere un singolo payload PES in diversi campioni. Ad esempio, se un payload PES è 20.000, verrà fornito in due campioni da 8.000 seguiti da un campione da 4K. Il demux non esamina il contenuto del flusso di byte. È il decodificatore ad analizzare le intestazioni di sequenza e cercare le modifiche al formato.

Quando il pin di output del filtro demux si connette al decodificatore, offre il tipo di supporto specificato al momento della creazione del pin. Poiché il demux non esamina il flusso di byte ES, non convalida il tipo di supporto. In teoria, un decodificatore MPEG-2 dovrebbe essere in grado di connettersi solo al tipo principale e al sottotipo compilati, per indicare il tipo di dati. Il decodificatore deve quindi esaminare le intestazioni di sequenza che arrivano nei campioni multimediali. Tuttavia, in pratica, molti decodificatori non si connetteranno a meno che il tipo di supporto non includa un blocco di formato completo.

Si supponga, ad esempio, che il 0x31 PID contenga il video del profilo principale MPEG-2. Come minimo, è necessario eseguire i passaggi seguenti.

Creare prima di tutto un tipo di supporto per il video MPEG-2. Lasciare da parte il blocco di formato per il momento:


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



Creare quindi un pin di output sul demux:


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



Eseguire quindi una query sul nuovo pin per **l'interfaccia IMPEG2PIDMap** e chiamare **MapPID**. Specificare il numero PID 0x30 e MEDIA \_ ELEMENTARY STREAM per i payload \_ PES.


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



Al termine, rilasciare tutte le interfacce:


```C++
pPin0->Release();
pDemux->Release();
```



Di seguito è riportato un esempio più completo di impostazione del tipo di supporto, incluso il blocco di formato. Questo esempio presuppone ancora un video del profilo principale MPEG-2. I dettagli variano a seconda del contenuto del flusso:


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

[Uso del demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



