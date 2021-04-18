---
description: Lettura dell'oggetto intestazione ASF di un file esistente
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Lettura dell'oggetto intestazione ASF di un file esistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309019"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a>Lettura dell'oggetto intestazione ASF di un file esistente

L'oggetto ContentInfo ASF archivia le informazioni che rappresentano gli oggetti intestazione ASF di un file multimediale. È necessario un oggetto ContentInfo popolato per leggere e analizzare un file ASF esistente.

Dopo aver creato l'oggetto ContentInfo chiamando la funzione [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , l'applicazione deve inizializzarla con le informazioni di intestazione del file ASF da leggere. Per popolare l'oggetto, chiamare [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).

**ParseHeader** richiede un buffer multimediale che contiene l'oggetto Header del file ASF. Un'opzione consiste nel riempire un buffer multimediale con l'oggetto intestazione per creare un flusso di byte per il file e quindi leggere i primi 30 byte di dati dal flusso di byte in un buffer multimediale. È quindi possibile ottenere le dimensioni passando i primi 24 byte dell'oggetto intestazione al metodo [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Una volta ottenute le dimensioni, è possibile leggere l'intero oggetto Header in un buffer multimediale e passarlo a **ParseHeader**. Il metodo avvia l'analisi in corrispondenza dell'offset dall'inizio del buffer multimediale specificato nel parametro *cbOffsetWithinHeader* .

Nell'esempio di codice seguente viene creato e inizializzato un oggetto ContentInfo per la lettura di un file ASF esistente contenuto in un flusso di byte. In primo luogo, viene definita una funzione helper che legge i dati da un flusso di byte e alloca un buffer multimediale per la memorizzazione dei dati:


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



Nell'esempio riportato di seguito viene letto l'oggetto intestazione ASF da un flusso di byte e viene popolato un oggetto con estensione ASF.


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



> [!Note]  
> In questi esempi viene usata la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto ContentInfo ASF](asf-contentinfo-object.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Recupero di informazioni da oggetti Header ASF](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



