---
description: Questo argomento descrive i passaggi per popolare le strutture necessarie per riprodurre dati audio in XAudio2.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 'Procedura: Caricare file di dati audio in XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659b4d8e106b6f0b2eb942505f99562f56fdada7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129766"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a><span data-ttu-id="5dd3d-103">Procedura: Caricare file di dati audio in XAudio2</span><span class="sxs-lookup"><span data-stu-id="5dd3d-103">How to: Load Audio Data Files in XAudio2</span></span>

> [!Note]  
> <span data-ttu-id="5dd3d-104">Questo contenuto si applica solo alle app desktop e richiede la revisione per funzionare in un'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="5dd3d-105">Consultare la documentazione per [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)e [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span><span class="sxs-lookup"><span data-stu-id="5dd3d-105">Please refer to the documentation for [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span></span> <span data-ttu-id="5dd3d-106">Vedere SoundFileReader. h/. cpp nell'esempio di BasicSound Windows 8 dalla [raccolta di esempi Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="5dd3d-106">See SoundFileReader.h/.cpp in the BasicSound Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="5dd3d-107">Questo argomento descrive i passaggi per popolare le strutture necessarie per riprodurre dati audio in XAudio2.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-107">This topic describes the steps to populate the structures required to play audio data in XAudio2.</span></span> <span data-ttu-id="5dd3d-108">I passaggi seguenti caricano i blocchi ' FMT ' è data ' di un file audio e li usano per popolare una struttura **WAVEFORMATEXTENSIBLE** e una struttura [**di \_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="5dd3d-108">The following steps load the 'fmt ' and 'data' chunks of an audio file, and uses them to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>

-   [<span data-ttu-id="5dd3d-109">Preparazione dell'analisi del file audio.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-109">Preparing to parse the audio file.</span></span>](#preparing-to-parse-the-audio-file)
-   [<span data-ttu-id="5dd3d-110">Popolamento di strutture XAudio2 con il contenuto dei blocchi RIFF.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-110">Populating XAudio2 structures with the contents of RIFF chunks.</span></span>](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a><span data-ttu-id="5dd3d-111">Preparazione dell'analisi del file audio</span><span class="sxs-lookup"><span data-stu-id="5dd3d-111">Preparing to parse the audio file</span></span>

<span data-ttu-id="5dd3d-112">I file audio supportati da XAudio2 usano il formato di file di interscambio risorse (RIFF).</span><span class="sxs-lookup"><span data-stu-id="5dd3d-112">Audio files supported by XAudio2 use the Resource Interchange File Format (RIFF).</span></span> <span data-ttu-id="5dd3d-113">Il RIFF è descritto nella panoramica del [formato del file di interscambio delle risorse (RIFF)](resource-interchange-file-format--riff-.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd3d-113">RIFF is described in the [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md) overview.</span></span> <span data-ttu-id="5dd3d-114">I dati audio in un file RIFF vengono caricati individuando il blocco del RIFF e quindi scorrendo il blocco per trovare i singoli blocchi contenuti nel blocco del RIFF.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-114">Audio data in a RIFF file is loaded by finding the RIFF chunk and then looping through the chunk to find individual chunks contained in the RIFF chunk.</span></span> <span data-ttu-id="5dd3d-115">Le funzioni seguenti sono esempi di codice per trovare i blocchi e caricare i dati contenuti nei blocchi.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-115">The following functions are examples of code to find chunks and load data contained in the chunks.</span></span>

-   <span data-ttu-id="5dd3d-116">Per trovare un blocco in un file RIFF:</span><span class="sxs-lookup"><span data-stu-id="5dd3d-116">To find a chunk in a RIFF file:</span></span>

    ```
    #ifdef _XBOX //Big-Endian
    #define fourccRIFF 'RIFF'
    #define fourccDATA 'data'
    #define fourccFMT 'fmt '
    #define fourccWAVE 'WAVE'
    #define fourccXWMA 'XWMA'
    #define fourccDPDS 'dpds'
    #endif

    #ifndef _XBOX //Little-Endian
    #define fourccRIFF 'FFIR'
    #define fourccDATA 'atad'
    #define fourccFMT ' tmf'
    #define fourccWAVE 'EVAW'
    #define fourccXWMA 'AMWX'
    #define fourccDPDS 'sdpd'
    #endif
    HRESULT FindChunk(HANDLE hFile, DWORD fourcc, DWORD & dwChunkSize, DWORD & dwChunkDataPosition)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );

        DWORD dwChunkType;
        DWORD dwChunkDataSize;
        DWORD dwRIFFDataSize = 0;
        DWORD dwFileType;
        DWORD bytesRead = 0;
        DWORD dwOffset = 0;

        while (hr == S_OK)
        {
            DWORD dwRead;
            if( 0 == ReadFile( hFile, &dwChunkType, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            if( 0 == ReadFile( hFile, &dwChunkDataSize, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            switch (dwChunkType)
            {
            case fourccRIFF:
                dwRIFFDataSize = dwChunkDataSize;
                dwChunkDataSize = 4;
                if( 0 == ReadFile( hFile, &dwFileType, sizeof(DWORD), &dwRead, NULL ) )
                    hr = HRESULT_FROM_WIN32( GetLastError() );
                break;

            default:
                if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, dwChunkDataSize, NULL, FILE_CURRENT ) )
                return HRESULT_FROM_WIN32( GetLastError() );            
            }

            dwOffset += sizeof(DWORD) * 2;
            
            if (dwChunkType == fourcc)
            {
                dwChunkSize = dwChunkDataSize;
                dwChunkDataPosition = dwOffset;
                return S_OK;
            }

            dwOffset += dwChunkDataSize;
            
            if (bytesRead >= dwRIFFDataSize) return S_FALSE;

        }

        return S_OK;
        
    }
    ```

    

-   <span data-ttu-id="5dd3d-117">Per leggere i dati in un blocco dopo che è stato individuato.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-117">To read data in a chunk after it has been located.</span></span>

    <span data-ttu-id="5dd3d-118">Una volta trovato un blocco desiderato, i relativi dati possono essere letti regolando il puntatore del file all'inizio della sezione di dati del blocco.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-118">Once a desired chunk is found, its data can be read by adjusting the file pointer to the beginning of the data section of the chunk.</span></span> <span data-ttu-id="5dd3d-119">Una funzione per leggere i dati da un blocco una volta trovati potrebbe avere un aspetto simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-119">A function to read the data from a chunk once it is found might look like this.</span></span>

    ```
    HRESULT ReadChunkData(HANDLE hFile, void * buffer, DWORD buffersize, DWORD bufferoffset)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, bufferoffset, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );
        DWORD dwRead;
        if( 0 == ReadFile( hFile, buffer, buffersize, &dwRead, NULL ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
        return hr;
    }
    ```

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a><span data-ttu-id="5dd3d-120">Popolamento di strutture XAudio2 con il contenuto dei blocchi RIFF</span><span class="sxs-lookup"><span data-stu-id="5dd3d-120">Populating XAudio2 structures with the contents of RIFF chunks</span></span>

<span data-ttu-id="5dd3d-121">Per consentire a XAudio2 di riprodurre audio con una voce di origine, è necessaria una struttura **WAVEFORMATEX** e una struttura di [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="5dd3d-121">In order for XAudio2 to play audio with a source voice, it needs a **WAVEFORMATEX** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="5dd3d-122">La struttura **WAVEFORMATEX** può essere una struttura più grande, ad esempio **WAVEFORMATEXTENSIBLE** che contiene una struttura **WAVEFORMATEX** come primo membro.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-122">The **WAVEFORMATEX** structure may be a larger structure such as **WAVEFORMATEXTENSIBLE** that contains a **WAVEFORMATEX** structure as its first member.</span></span> <span data-ttu-id="5dd3d-123">Per ulteriori informazioni, vedere la pagina di riferimento di **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="5dd3d-123">See the **WAVEFORMATEX** reference page for more information.</span></span>

<span data-ttu-id="5dd3d-124">In questo esempio viene usato un **WAVEFORMATEXTENSIBLE** per consentire il caricamento di file audio PCM con più di due canali.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-124">In this example a **WAVEFORMATEXTENSIBLE** is being used to allow loading of PCM audio files with more than two channels.</span></span>

<span data-ttu-id="5dd3d-125">La procedura seguente illustra l'uso delle funzioni descritte in precedenza per popolare una struttura **WAVEFORMATEXTENSIBLE** e una struttura di [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="5dd3d-125">The following steps illustrate using the functions described above to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="5dd3d-126">In questo caso, il file audio caricato contiene dati PCM e conterrà solo i blocchi ' RIFF ',' FMT ' è data '.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-126">In this case, the audio file being loaded contains PCM data, and will only contain a 'RIFF', 'fmt ', and 'data' chunk.</span></span> <span data-ttu-id="5dd3d-127">Altri formati possono contenere tipi di blocchi aggiuntivi, come descritto in [formato di file di interscambio risorse (RIFF)](resource-interchange-file-format--riff-.md).</span><span class="sxs-lookup"><span data-stu-id="5dd3d-127">Other formats may contain additional chunk types as described in [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md).</span></span>

1.  <span data-ttu-id="5dd3d-128">Dichiarare le strutture [**del \_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEXTENSIBLE** e XAUDIO2.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-128">Declare **WAVEFORMATEXTENSIBLE** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structures.</span></span>
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  <span data-ttu-id="5dd3d-129">Aprire il file audio con CreateFile.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-129">Open the audio file with CreateFile.</span></span>
    ```
    #ifdef _XBOX
    char * strFileName = "game:\\media\\MusicMono.wav";
    #else
    TCHAR * strFileName = _TEXT("media\\MusicMono.wav");
    #endif
    // Open the file
    HANDLE hFile = CreateFile(
        strFileName,
        GENERIC_READ,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        0,
        NULL );

    if( INVALID_HANDLE_VALUE == hFile )
        return HRESULT_FROM_WIN32( GetLastError() );

    if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
        return HRESULT_FROM_WIN32( GetLastError() );
    ```

    

3.  <span data-ttu-id="5dd3d-130">Individuare il blocco "RIFF" nel file audio e controllare il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-130">Locate the 'RIFF' chunk in the audio file, and check the file type.</span></span>
    ```
    DWORD dwChunkSize;
    DWORD dwChunkPosition;
    //check the file type, should be fourccWAVE or 'XWMA'
    FindChunk(hFile,fourccRIFF,dwChunkSize, dwChunkPosition );
    DWORD filetype;
    ReadChunkData(hFile,&filetype,sizeof(DWORD),dwChunkPosition);
    if (filetype != fourccWAVE)
        return S_FALSE;
    ```

    

4.  <span data-ttu-id="5dd3d-131">Individuare il blocco ' FMT ' e copiarne il contenuto in una struttura **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="5dd3d-131">Locate the 'fmt ' chunk, and copy its contents into a **WAVEFORMATEXTENSIBLE** structure.</span></span>
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  <span data-ttu-id="5dd3d-132">Individuare il blocco "data" e leggerne il contenuto in un buffer.</span><span class="sxs-lookup"><span data-stu-id="5dd3d-132">Locate the 'data' chunk, and read its contents into a buffer.</span></span>
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  <span data-ttu-id="5dd3d-133">Popola una struttura di [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="5dd3d-133">Populate an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5dd3d-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5dd3d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dd3d-135">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="5dd3d-135">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="5dd3d-136">Procedura: Riprodurre un suono con XAudio2</span><span class="sxs-lookup"><span data-stu-id="5dd3d-136">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="5dd3d-137">Guida di riferimento alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="5dd3d-137">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
