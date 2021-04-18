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
# <a name="generating-a-new-asf-header-object"></a><span data-ttu-id="e299a-103">Generazione di un nuovo oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="e299a-103">Generating a New ASF Header Object</span></span>

<span data-ttu-id="e299a-104">Per convertire le informazioni contenute nell'oggetto ContentInfo in un formato oggetto intestazione ASF binario, l'applicazione deve chiamare [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="e299a-104">To convert the information contained in the ContentInfo object to a binary ASF Header Object format, the application must call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="e299a-105">Questa chiamata deve essere eseguita dopo la generazione dei pacchetti di dati e l'oggetto ContentInfo contiene informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="e299a-105">This call must be made after the data packets are generated and the ContentInfo object contains updated information.</span></span> <span data-ttu-id="e299a-106">**GenerateHeader** restituisce un puntatore a un buffer multimediale che contiene le informazioni di intestazione nel formato valido.</span><span class="sxs-lookup"><span data-stu-id="e299a-106">**GenerateHeader** returns a pointer to a media buffer that contains the header information in the valid format.</span></span> <span data-ttu-id="e299a-107">L'applicazione può quindi scrivere i dati a cui punta il buffer multimediale all'inizio di un nuovo file ASF.</span><span class="sxs-lookup"><span data-stu-id="e299a-107">The application can then write the data, pointed to by the media buffer, at the beginning of a new ASF file.</span></span>

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a><span data-ttu-id="e299a-108">Per scrivere un nuovo oggetto Header usando l'oggetto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="e299a-108">To write a new Header Object by using the ContentInfo object</span></span>

1.  <span data-ttu-id="e299a-109">Chiamare [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) per creare un oggetto ContentInfo vuoto.</span><span class="sxs-lookup"><span data-stu-id="e299a-109">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="e299a-110">Chiamare [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per fornire l'oggetto profilo all'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="e299a-110">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to supply the profile object to the ContentInfo object.</span></span> <span data-ttu-id="e299a-111">Per informazioni sulla creazione di profili, vedere [creazione di un profilo ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="e299a-111">For information about creating profiles, see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
3.  <span data-ttu-id="e299a-112">Chiamare [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) e passare **null** nel parametro *pIHeader* e ricevere le dimensioni dell'oggetto ContentInfo popolato nel parametro *pcbHeader* .</span><span class="sxs-lookup"><span data-stu-id="e299a-112">Call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) and pass **NULL** in the *pIHeader* parameter and receive the size of the populated ContentInfo object in the *pcbHeader* parameter.</span></span> <span data-ttu-id="e299a-113">L'applicazione può usare questo valore per allocare memoria o il buffer multimediale che conterrà l'oggetto intestazione.</span><span class="sxs-lookup"><span data-stu-id="e299a-113">The application can use this value to allocate memory or the media buffer that will contain the Header Object.</span></span>

    <span data-ttu-id="e299a-114">Le dimensioni dell'intestazione ricevute includono la dimensione della spaziatura interna, che viene modificata a seconda delle dimensioni effettive degli oggetti intestazione.</span><span class="sxs-lookup"><span data-stu-id="e299a-114">The header size received includes the padding size, which is adjusted depending on the actual size of the header objects.</span></span> <span data-ttu-id="e299a-115">Le dimensioni massime degli oggetti intestazione sono 10 MB.</span><span class="sxs-lookup"><span data-stu-id="e299a-115">The maximum size of the header objects is 10 MB.</span></span> <span data-ttu-id="e299a-116">Se la dimensione supera questo valore, **GenerateHeader** ha esito negativo con l' \_ errore INVALIDDATA di MF E \_ ASF \_ .</span><span class="sxs-lookup"><span data-stu-id="e299a-116">If the size exceeds this value, **GenerateHeader** fails with the MF\_E\_ASF\_INVALIDDATA error.</span></span>

4.  <span data-ttu-id="e299a-117">Chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) per creare un buffer multimediale con le dimensioni ricevute nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="e299a-117">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer of the received size in step 3.</span></span>
5.  <span data-ttu-id="e299a-118">Chiamare di nuovo **GenerateHeader** per generare il nuovo oggetto intestazione ASF dall'oggetto ContentInfo nel buffer multimediale creato nel passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="e299a-118">Call **GenerateHeader** again to generate the new ASF Header Object from the ContentInfo object in the media buffer created in step 4.</span></span>

    <span data-ttu-id="e299a-119">La lunghezza dei dati nel buffer multimediale viene aggiornata e la nuova dimensione viene restituita nel parametro *pcbHeader* .</span><span class="sxs-lookup"><span data-stu-id="e299a-119">The length of the data in the media buffer is updated and the new size is returned in the *pcbHeader* parameter.</span></span>

6.  <span data-ttu-id="e299a-120">Scrivere il contenuto del buffer multimediale all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="e299a-120">Write the contents of the media buffer at the beginning of the file.</span></span> <span data-ttu-id="e299a-121">L'applicazione può usare il flusso di byte per eseguire l'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="e299a-121">The application can use the byte stream to perform the writing operation.</span></span> <span data-ttu-id="e299a-122">Per un esempio di codice, vedere [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="e299a-122">For example code, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>

### <a name="example"></a><span data-ttu-id="e299a-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="e299a-123">Example</span></span>

<span data-ttu-id="e299a-124">Nell'esempio di codice seguente viene illustrato come creare un oggetto ContentInfo e generare un buffer multimediale per archiviare il nuovo oggetto intestazione.</span><span class="sxs-lookup"><span data-stu-id="e299a-124">The following example code shows how to create a ContentInfo object and generate a media buffer to store the new Header Object.</span></span> <span data-ttu-id="e299a-125">Per un esempio completo in cui viene usato questo codice, vedere [esercitazione: copia di flussi ASF da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="e299a-125">For a complete example that uses this code, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e299a-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e299a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e299a-127">Scrittura di un oggetto intestazione ASF per un nuovo file</span><span class="sxs-lookup"><span data-stu-id="e299a-127">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



