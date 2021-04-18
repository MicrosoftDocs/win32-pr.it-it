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
# <a name="reading-the-asf-header-object-of-an-existing-file"></a><span data-ttu-id="29454-103">Lettura dell'oggetto intestazione ASF di un file esistente</span><span class="sxs-lookup"><span data-stu-id="29454-103">Reading the ASF Header Object of an Existing File</span></span>

<span data-ttu-id="29454-104">L'oggetto ContentInfo ASF archivia le informazioni che rappresentano gli oggetti intestazione ASF di un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="29454-104">The ASF ContentInfo object stores information that represents the ASF Header Objects of a media file.</span></span> <span data-ttu-id="29454-105">È necessario un oggetto ContentInfo popolato per leggere e analizzare un file ASF esistente.</span><span class="sxs-lookup"><span data-stu-id="29454-105">A populated ContentInfo object is required in order to read and parse an existing ASF file.</span></span>

<span data-ttu-id="29454-106">Dopo aver creato l'oggetto ContentInfo chiamando la funzione [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , l'applicazione deve inizializzarla con le informazioni di intestazione del file ASF da leggere.</span><span class="sxs-lookup"><span data-stu-id="29454-106">After creating the ContentInfo object by calling the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function, the application must initialize it with header information from the ASF file that is to be read.</span></span> <span data-ttu-id="29454-107">Per popolare l'oggetto, chiamare [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="29454-107">To populate the object, call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span>

<span data-ttu-id="29454-108">**ParseHeader** richiede un buffer multimediale che contiene l'oggetto Header del file ASF.</span><span class="sxs-lookup"><span data-stu-id="29454-108">**ParseHeader** requires a media buffer that contains the Header Object of the ASF file.</span></span> <span data-ttu-id="29454-109">Un'opzione consiste nel riempire un buffer multimediale con l'oggetto intestazione per creare un flusso di byte per il file e quindi leggere i primi 30 byte di dati dal flusso di byte in un buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="29454-109">One option is to fill a media buffer with the Header Object to create a byte stream for the file and then read the first 30 bytes of data from the byte stream into a media buffer.</span></span> <span data-ttu-id="29454-110">È quindi possibile ottenere le dimensioni passando i primi 24 byte dell'oggetto intestazione al metodo [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="29454-110">You can then get the size by passing the first 24 bytes of the Header Object to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="29454-111">Una volta ottenute le dimensioni, è possibile leggere l'intero oggetto Header in un buffer multimediale e passarlo a **ParseHeader**.</span><span class="sxs-lookup"><span data-stu-id="29454-111">After getting the size, you can read the entire Header Object in a media buffer and pass it to **ParseHeader**.</span></span> <span data-ttu-id="29454-112">Il metodo avvia l'analisi in corrispondenza dell'offset dall'inizio del buffer multimediale specificato nel parametro *cbOffsetWithinHeader* .</span><span class="sxs-lookup"><span data-stu-id="29454-112">The method starts parsing at the offset from the start of the media buffer specified in the *cbOffsetWithinHeader* parameter.</span></span>

<span data-ttu-id="29454-113">Nell'esempio di codice seguente viene creato e inizializzato un oggetto ContentInfo per la lettura di un file ASF esistente contenuto in un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="29454-113">The following example code creates and initializes a ContentInfo object for reading an existing ASF file contained in a byte stream.</span></span> <span data-ttu-id="29454-114">In primo luogo, viene definita una funzione helper che legge i dati da un flusso di byte e alloca un buffer multimediale per la memorizzazione dei dati:</span><span class="sxs-lookup"><span data-stu-id="29454-114">First, we define a helper function that reads data from a byte stream and allocates a media buffer to hold the data:</span></span>


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



<span data-ttu-id="29454-115">Nell'esempio riportato di seguito viene letto l'oggetto intestazione ASF da un flusso di byte e viene popolato un oggetto con estensione ASF.</span><span class="sxs-lookup"><span data-stu-id="29454-115">The next example reads the ASF Header Object from a byte stream and populates an ASF ContentInfo object.</span></span>


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
> <span data-ttu-id="29454-116">In questi esempi viene usata la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="29454-116">These examples use the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="29454-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29454-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29454-118">Oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="29454-118">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="29454-119">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="29454-119">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="29454-120">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29454-120">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="29454-121">Recupero di informazioni da oggetti Header ASF</span><span class="sxs-lookup"><span data-stu-id="29454-121">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



