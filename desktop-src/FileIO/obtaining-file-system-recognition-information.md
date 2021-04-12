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
# <a name="obtaining-file-system-recognition-information"></a><span data-ttu-id="fbf51-103">Recupero delle informazioni di riconoscimento del file System</span><span class="sxs-lookup"><span data-stu-id="fbf51-103">Obtaining File System Recognition Information</span></span>

<span data-ttu-id="fbf51-104">Il [riconoscimento del file System](file-system-recognition.md) è la possibilità di riconoscere i supporti di archiviazione che contengono un layout file System/volume valido che non è ancora stato definito, ma il supporto è in grado di identificarsi con la presenza della struttura di riconoscimento definita internamente da Windows.</span><span class="sxs-lookup"><span data-stu-id="fbf51-104">[File system recognition](file-system-recognition.md) is the ability to recognize storage media that contain a valid file system/volume layout that has not been defined yet, but the media is able to identify itself through the presence of the recognition structure defined internally by Windows.</span></span>

<span data-ttu-id="fbf51-105">Poiché nessun file system esistente riconoscerà un nuovo layout del disco, il file system "RAW" installerà il volume e fornirà l'accesso diretto a livello di blocco.</span><span class="sxs-lookup"><span data-stu-id="fbf51-105">Because no existing file system will recognize a new disk layout, the "RAW" file system will mount the volume and provide direct block level access.</span></span> <span data-ttu-id="fbf51-106">La file system "RAW", incorporata in *NtosKrnl*, potrà leggere la struttura di riconoscimento file System e fornire alle applicazioni l'accesso a tali strutture tramite la richiesta di controllo file System il [**\_ \_ \_ \_ riconoscimento del file System di query FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="fbf51-106">The "RAW" file system, incorporated in *NtosKrnl*, will have the ability to read the file system recognition structure and provide applications access to such structures through the file system control request [**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), shown in the following example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fbf51-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fbf51-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbf51-108">Riconoscimento del file System</span><span class="sxs-lookup"><span data-stu-id="fbf51-108">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="fbf51-109">**struttura di riconoscimento del FILE \_ System \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fbf51-109">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> <dt>

[<span data-ttu-id="fbf51-110">**\_riconoscimento del \_ file \_ System di query \_ FSCTL**</span><span class="sxs-lookup"><span data-stu-id="fbf51-110">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
