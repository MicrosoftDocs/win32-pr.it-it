---
description: Generazione di un nuovo oggetto intestazione ASF
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Generazione di un nuovo oggetto intestazione ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524513"
---
# <a name="generating-a-new-asf-header-object"></a>Generazione di un nuovo oggetto intestazione ASF

Per convertire le informazioni contenute nell'oggetto ContentInfo in un formato oggetto intestazione ASF binario, l'applicazione deve chiamare [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Questa chiamata deve essere eseguita dopo la generazione dei pacchetti di dati e l'oggetto ContentInfo contiene informazioni aggiornate. **GenerateHeader** restituisce un puntatore a un buffer multimediale che contiene le informazioni di intestazione nel formato valido. L'applicazione può quindi scrivere i dati a cui punta il buffer multimediale all'inizio di un nuovo file ASF.

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a>Per scrivere un nuovo oggetto Header usando l'oggetto ContentInfo

1.  Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare un oggetto ContentInfo vuoto.
2.  Chiamare [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per fornire l'oggetto profilo all'oggetto ContentInfo. Per informazioni sulla creazione di profili, vedere [creazione di un profilo ASF](creating-an-asf-profile.md).
3.  Chiamare [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) e passare **null** nel parametro *pIHeader* e ricevere le dimensioni dell'oggetto ContentInfo popolato nel parametro *pcbHeader* . L'applicazione può usare questo valore per allocare memoria o il buffer multimediale che conterrà l'oggetto intestazione.

    Le dimensioni dell'intestazione ricevute includono la dimensione della spaziatura interna, che viene modificata a seconda delle dimensioni effettive degli oggetti intestazione. Le dimensioni massime degli oggetti intestazione sono 10 MB. Se la dimensione supera questo valore, **GenerateHeader** ha esito negativo con l' \_ errore INVALIDDATA di MF E \_ ASF \_ .

4.  Chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) per creare un buffer multimediale con le dimensioni ricevute nel passaggio 3.
5.  Chiamare di nuovo **GenerateHeader** per generare il nuovo oggetto intestazione ASF dall'oggetto ContentInfo nel buffer multimediale creato nel passaggio 4.

    La lunghezza dei dati nel buffer multimediale viene aggiornata e la nuova dimensione viene restituita nel parametro *pcbHeader* .

6.  Scrivere il contenuto del buffer multimediale all'inizio del file. L'applicazione può usare il flusso di byte per eseguire l'operazione di scrittura. Per un esempio di codice, vedere [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

### <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come creare un oggetto ContentInfo e generare un buffer multimediale per archiviare il nuovo oggetto intestazione. Per un esempio completo in cui viene usato questo codice, vedere [esercitazione: copia di flussi ASF da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md).


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un oggetto intestazione ASF per un nuovo file](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



