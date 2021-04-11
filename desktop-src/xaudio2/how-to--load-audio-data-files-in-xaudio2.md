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
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>Procedura: Caricare file di dati audio in XAudio2

> [!Note]  
> Questo contenuto si applica solo alle app desktop e richiede la revisione per funzionare in un'app di Windows Store. Consultare la documentazione per [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)e [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex). Vedere SoundFileReader. h/. cpp nell'esempio di BasicSound Windows 8 dalla [raccolta di esempi Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).

 

Questo argomento descrive i passaggi per popolare le strutture necessarie per riprodurre dati audio in XAudio2. I passaggi seguenti caricano i blocchi ' FMT ' è data ' di un file audio e li usano per popolare una struttura **WAVEFORMATEXTENSIBLE** e una struttura [**di \_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .

-   [Preparazione dell'analisi del file audio.](#preparing-to-parse-the-audio-file)
-   [Popolamento di strutture XAudio2 con il contenuto dei blocchi RIFF.](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>Preparazione dell'analisi del file audio

I file audio supportati da XAudio2 usano il formato di file di interscambio risorse (RIFF). Il RIFF è descritto nella panoramica del [formato del file di interscambio delle risorse (RIFF)](resource-interchange-file-format--riff-.md) . I dati audio in un file RIFF vengono caricati individuando il blocco del RIFF e quindi scorrendo il blocco per trovare i singoli blocchi contenuti nel blocco del RIFF. Le funzioni seguenti sono esempi di codice per trovare i blocchi e caricare i dati contenuti nei blocchi.

-   Per trovare un blocco in un file RIFF:

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

    

-   Per leggere i dati in un blocco dopo che è stato individuato.

    Una volta trovato un blocco desiderato, i relativi dati possono essere letti regolando il puntatore del file all'inizio della sezione di dati del blocco. Una funzione per leggere i dati da un blocco una volta trovati potrebbe avere un aspetto simile al seguente.

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>Popolamento di strutture XAudio2 con il contenuto dei blocchi RIFF

Per consentire a XAudio2 di riprodurre audio con una voce di origine, è necessaria una struttura **WAVEFORMATEX** e una struttura di [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . La struttura **WAVEFORMATEX** può essere una struttura più grande, ad esempio **WAVEFORMATEXTENSIBLE** che contiene una struttura **WAVEFORMATEX** come primo membro. Per ulteriori informazioni, vedere la pagina di riferimento di **WAVEFORMATEX** .

In questo esempio viene usato un **WAVEFORMATEXTENSIBLE** per consentire il caricamento di file audio PCM con più di due canali.

La procedura seguente illustra l'uso delle funzioni descritte in precedenza per popolare una struttura **WAVEFORMATEXTENSIBLE** e una struttura di [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . In questo caso, il file audio caricato contiene dati PCM e conterrà solo i blocchi ' RIFF ',' FMT ' è data '. Altri formati possono contenere tipi di blocchi aggiuntivi, come descritto in [formato di file di interscambio risorse (RIFF)](resource-interchange-file-format--riff-.md).

1.  Dichiarare le strutture [**del \_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEXTENSIBLE** e XAUDIO2.
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  Aprire il file audio con CreateFile.
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

    

3.  Individuare il blocco "RIFF" nel file audio e controllare il tipo di file.
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

    

4.  Individuare il blocco ' FMT ' e copiarne il contenuto in una struttura **WAVEFORMATEXTENSIBLE** .
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  Individuare il blocco "data" e leggerne il contenuto in un buffer.
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  Popola una struttura di [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Procedura: Riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Guida di riferimento alla programmazione di XAudio2](programming-reference.md)
</dt> </dl>

 

 
