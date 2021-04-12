---
description: Il riconoscimento del file System è la possibilità di riconoscere i supporti di archiviazione che contengono un layout file system/volume valido che non è ancora stato definito, ma il supporto è in grado di identificarsi con la presenza della struttura di riconoscimento definita internamente da Windows.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Recupero delle informazioni di riconoscimento del file System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cafa9f1c7cf6cbbe11d434aff3db424a1cd0a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344291"
---
# <a name="obtaining-file-system-recognition-information"></a>Recupero delle informazioni di riconoscimento del file System

Il [riconoscimento del file System](file-system-recognition.md) è la possibilità di riconoscere i supporti di archiviazione che contengono un layout file System/volume valido che non è ancora stato definito, ma il supporto è in grado di identificarsi con la presenza della struttura di riconoscimento definita internamente da Windows.

Poiché nessun file system esistente riconoscerà un nuovo layout del disco, il file system "RAW" installerà il volume e fornirà l'accesso diretto a livello di blocco. La file system "RAW", incorporata in *NtosKrnl*, potrà leggere la struttura di riconoscimento file System e fornire alle applicazioni l'accesso a tali strutture tramite la richiesta di controllo file System il [**\_ \_ \_ \_ riconoscimento del file System di query FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), illustrato nell'esempio seguente.


```C++
STDMETHODIMP CheckFileSystem(
    PCWSTR pcwszDrive
    ) 
{
    HRESULT hr = S_OK;
    HANDLE  hDisk = INVALID_HANDLE_VALUE;
    BOOL    fResult = FALSE;    
    ULONG   BytesReturned = 0;    
    FILE_SYSTEM_RECOGNITION_INFORMATION     FsRi = {0};
    
    //
    // Open the target, for example "\\.\C:"
    //
    wprintf( L"CreateFile on %s...", pcwszDrive );
    hDisk = CreateFile( pcwszDrive, 
                        FILE_READ_ATTRIBUTES|SYNCHRONIZE|FILE_TRAVERSE,                        
                        FILE_SHARE_READ|FILE_SHARE_WRITE,
                        NULL, OPEN_EXISTING, 0, NULL );    
    if( hDisk == INVALID_HANDLE_VALUE ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"CreateFile failed on %s, GLE = 0x%x\n", pcwszDrive, GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"\nPress Any Key to send down the FSCTL\n" );
    _getwch();

    //
    // Send down the FSCTL
    //
    wprintf( L"Calling DeviceIoControl( FSCTL_QUERY_FILE_SYSTEM_RECOGNITION ) " );
    
    fResult = DeviceIoControl( hDisk, 
                               FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, 
                               NULL, 
                               0, 
                               &FsRi, 
                               sizeof(FsRi), 
                               &BytesReturned, 
                               NULL );
    if( !fResult ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"failed GLE = 0x%x\n", GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION returned success.\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION retrieved \"%S\".\n",
              FsRi.FileSystem );

exit:

    if( hDisk != INVALID_HANDLE_VALUE ) 
    {
        CloseHandle( hDisk );
        hDisk = INVALID_HANDLE_VALUE;
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riconoscimento del file System](file-system-recognition.md)
</dt> <dt>

[**struttura di riconoscimento del FILE \_ System \_ \_**](file-system-recognition-structure.md)
</dt> <dt>

[**\_riconoscimento del \_ file \_ System di query \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
