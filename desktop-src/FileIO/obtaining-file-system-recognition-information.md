---
description: Il riconoscimento del file system è la possibilità di riconoscere i supporti di archiviazione che contengono un layout file system/volume valido che non è stato ancora definito, ma il supporto è in grado di identificarsi tramite la presenza della struttura di riconoscimento definita internamente da Windows.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Recupero di informazioni di riconoscimento del file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c10b538f9e98ecab3f8f8f72784ef658c068f780388dc7b600be68b76380757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148507"
---
# <a name="obtaining-file-system-recognition-information"></a>Recupero di informazioni di riconoscimento del file system

Il riconoscimento del file [system](file-system-recognition.md) è la possibilità di riconoscere i supporti di archiviazione che contengono un layout di file system/volume valido che non è stato ancora definito, ma il supporto è in grado di identificarsi tramite la presenza della struttura di riconoscimento definita internamente da Windows.

Poiché nessun file system riconoscerà un nuovo layout del disco, il file system "RAW" monta il volume e fornisce l'accesso diretto a livello di blocco. Il file system "RAW", incorporato in *NtosKrnl,* sarà in grado di leggere la struttura di riconoscimento file system e fornire alle applicazioni l'accesso a tali strutture tramite la richiesta di controllo [**file system FSCTL \_ QUERY FILE SYSTEM \_ \_ \_ RECOGNITION,**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)come illustrato nell'esempio seguente.


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

[Riconoscimento del file system](file-system-recognition.md)
</dt> <dt>

[**STRUTTURA DI RICONOSCIMENTO DEL FILE \_ \_ \_ SYSTEM**](file-system-recognition-structure.md)
</dt> <dt>

[**RICONOSCIMENTO DEL \_ FILE SYSTEM DI QUERY \_ \_ \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
