---
description: Generazione di un nuovo oggetto intestazione ASF
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Generazione di un nuovo oggetto intestazione ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df567c1c530fa902b002c46ff18aa560cfa2b0b887ee6893a17dfe7a2904796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063628"
---
# <a name="generating-a-new-asf-header-object"></a>Generazione di un nuovo oggetto intestazione ASF

Per convertire le informazioni contenute nell'oggetto ContentInfo in un formato ASF Header Object binario, l'applicazione deve chiamare [**IMFASFContentInfo::GenerateHeader.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) Questa chiamata deve essere effettuata dopo che i pacchetti di dati sono stati generati e l'oggetto ContentInfo contiene informazioni aggiornate. **GenerateHeader** restituisce un puntatore a un buffer multimediale che contiene le informazioni sull'intestazione nel formato valido. L'applicazione può quindi scrivere i dati, a cui punta il buffer multimediale, all'inizio di un nuovo file ASF.

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a>Per scrivere un nuovo oggetto Header usando l'oggetto ContentInfo

1.  Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare un oggetto ContentInfo vuoto.
2.  Chiamare [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per fornire l'oggetto profilo all'oggetto ContentInfo. Per informazioni sulla creazione di profili, vedere [Creazione di un profilo ASF.](creating-an-asf-profile.md)
3.  Chiamare [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) e passare **NULL** nel parametro *pIHeader* e ricevere le dimensioni dell'oggetto ContentInfo popolato nel *parametro pcbHeader.* L'applicazione può usare questo valore per allocare memoria o il buffer multimediale che conterrà l'oggetto Intestazione.

    Le dimensioni dell'intestazione ricevute includono la dimensione della spaziatura interna, che viene regolata in base alle dimensioni effettive degli oggetti intestazione. La dimensione massima degli oggetti intestazione è 10 MB. Se le dimensioni superano questo valore, **GenerateHeader** ha esito negativo con l'errore INVALIDDATA di MF \_ E \_ \_ ASF.

4.  Chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) per creare un buffer multimediale delle dimensioni ricevute nel passaggio 3.
5.  Chiamare **di nuovo GenerateHeader** per generare il nuovo oggetto intestazione ASF dall'oggetto ContentInfo nel buffer multimediale creato nel passaggio 4.

    La lunghezza dei dati nel buffer multimediale viene aggiornata e le nuove dimensioni vengono restituite nel *parametro pcbHeader.*

6.  Scrivere il contenuto del buffer multimediale all'inizio del file. L'applicazione può usare il flusso di byte per eseguire l'operazione di scrittura. Per un codice di esempio, [**vedere IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

### <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come creare un oggetto ContentInfo e generare un buffer multimediale per archiviare il nuovo oggetto Header. Per un esempio completo che usa questo codice, vedere Esercitazione: Copia di file [ASF Flussi da un file a un altro.](tutorial--copying-asf-streams-from-one-file-to-another.md)


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

 

 



