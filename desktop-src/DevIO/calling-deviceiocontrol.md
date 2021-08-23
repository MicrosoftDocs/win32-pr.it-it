---
description: Chiamata di DeviceIoControl
ms.assetid: b4dbda89-effb-43f7-b3cc-774db57862a9
title: Chiamata di DeviceIoControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1372adc551d7816c047823b70a7541fa50318632ff7ea593f70896ceffc4f80c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642091"
---
# <a name="calling-deviceiocontrol"></a>Chiamata di DeviceIoControl

Un'applicazione può usare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) per eseguire operazioni di input e output dirette su un'unità disco floppy, un'unità disco rigido, un'unità nastro o un'unità CD-ROM. Per un elenco dei codici di controllo standard inclusi nella documentazione dell'SDK, vedere la sezione Osservazioni di **DeviceIoControl.**

Nell'esempio seguente viene illustrato come recuperare informazioni sulla prima unità fisica nel sistema. Usa la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per recuperare l'handle del dispositivo per la prima unità fisica e quindi usa [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con il codice di controllo [IOCTL \_ DISK GET DRIVE \_ \_ \_ GEOMETRY](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry) per riempire una struttura [**DISK \_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) con informazioni sull'unità.


```C++
#define UNICODE 1
#define _UNICODE 1

/* The code of interest is in the subroutine GetDriveGeometry. The 
   code in main shows how to interpret the results of the call. */

#include <windows.h>
#include <winioctl.h>
#include <stdio.h>

#define wszDrive L"\\\\.\\PhysicalDrive0"

BOOL GetDriveGeometry(LPWSTR wszPath, DISK_GEOMETRY *pdg)
{
  HANDLE hDevice = INVALID_HANDLE_VALUE;  // handle to the drive to be examined 
  BOOL bResult   = FALSE;                 // results flag
  DWORD junk     = 0;                     // discard results

  hDevice = CreateFileW(wszPath,          // drive to open
                        0,                // no access to the drive
                        FILE_SHARE_READ | // share mode
                        FILE_SHARE_WRITE, 
                        NULL,             // default security attributes
                        OPEN_EXISTING,    // disposition
                        0,                // file attributes
                        NULL);            // do not copy file attributes

  if (hDevice == INVALID_HANDLE_VALUE)    // cannot open the drive
  {
    return (FALSE);
  }

  bResult = DeviceIoControl(hDevice,                       // device to be queried
                            IOCTL_DISK_GET_DRIVE_GEOMETRY, // operation to perform
                            NULL, 0,                       // no input buffer
                            pdg, sizeof(*pdg),            // output buffer
                            &junk,                         // # bytes returned
                            (LPOVERLAPPED) NULL);          // synchronous I/O

  CloseHandle(hDevice);

  return (bResult);
}

int wmain(int argc, wchar_t *argv[])
{
  DISK_GEOMETRY pdg = { 0 }; // disk drive geometry structure
  BOOL bResult = FALSE;      // generic results flag
  ULONGLONG DiskSize = 0;    // size of the drive, in bytes

  bResult = GetDriveGeometry (wszDrive, &pdg);

  if (bResult) 
  {
    wprintf(L"Drive path      = %ws\n",   wszDrive);
    wprintf(L"Cylinders       = %I64d\n", pdg.Cylinders);
    wprintf(L"Tracks/cylinder = %ld\n",   (ULONG) pdg.TracksPerCylinder);
    wprintf(L"Sectors/track   = %ld\n",   (ULONG) pdg.SectorsPerTrack);
    wprintf(L"Bytes/sector    = %ld\n",   (ULONG) pdg.BytesPerSector);

    DiskSize = pdg.Cylinders.QuadPart * (ULONG)pdg.TracksPerCylinder *
               (ULONG)pdg.SectorsPerTrack * (ULONG)pdg.BytesPerSector;
    wprintf(L"Disk size       = %I64d (Bytes)\n"
            L"                = %.2f (Gb)\n", 
            DiskSize, (double) DiskSize / (1024 * 1024 * 1024));
  } 
  else 
  {
    wprintf (L"GetDriveGeometry failed. Error %ld.\n", GetLastError ());
  }

  return ((int)bResult);
}
```



 

 
