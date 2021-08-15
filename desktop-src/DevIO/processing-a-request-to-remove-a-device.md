---
description: Un'applicazione riceve un evento del dispositivo DBT DEVICEQUERYREMOVE quando una funzionalità del sistema ha deciso \_ di rimuovere un dispositivo specificato.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Elaborazione di una richiesta di rimozione di un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6432ba2709dd05589acd5f8e0a2d1de6547216c9d24d4c9d742b9ad6dcc838e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956780"
---
# <a name="processing-a-request-to-remove-a-device"></a>Elaborazione di una richiesta di rimozione di un dispositivo

Un'applicazione riceve un evento del dispositivo [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) quando una funzionalità del sistema ha deciso di rimuovere un dispositivo specificato. Quando l'applicazione riceve questo evento, deve determinare se usa il dispositivo specificato e annullare o preparare la rimozione.

Nell'esempio seguente un'applicazione gestisce un handle aperto, hFile, per il file o il dispositivo rappresentato da FileName. L'applicazione si registra per la notifica degli eventi del dispositivo nel dispositivo sottostante chiamando la funzione [**RegisterDeviceNotification,**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) usando un filtro di notifica di tipo **\_ DBT DEVTYP \_ HANDLE** e specificando la variabile hFile nel membro **\_ dell'handle dbch** del filtro.

L'applicazione elabora [l'evento del dispositivo DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) chiudendo l'handle di file aperto per il dispositivo da rimuovere. Nel caso in cui la rimozione di questo dispositivo viene annullata, l'applicazione elabora l'evento del dispositivo [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) per riaprire l'handle al dispositivo. Dopo la rimozione del dispositivo dal sistema, l'applicazione elabora gli eventi del dispositivo [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) e [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) annullando la registrazione dell'handle di notifica per il dispositivo e chiudendo tutti gli handle ancora aperti al dispositivo.


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
  // ...

INT_PTR WINAPI WinProcCallback( HWND hWnd,
                                UINT message,
                                WPARAM wParam,
                                LPARAM lParam )
{
  LPCTSTR FileName = NULL;              // path to the file or device of interest
  HANDLE  hFile = INVALID_HANDLE_VALUE; // handle to the file or device

  PDEV_BROADCAST_HDR    pDBHdr;
  PDEV_BROADCAST_HANDLE pDBHandle;
  TCHAR szMsg[80];

  switch (message)
  {
  //...
  case WM_DEVICECHANGE:
    switch (wParam)
    {
      case DBT_DEVICEQUERYREMOVE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // A request has been made to remove the device;
            // close any open handles to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }
        }
        return TRUE;

      case DBT_DEVICEQUERYREMOVEFAILED:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            // Removal of the device has failed;
            // reopen a handle to the file or device

            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            hFile = CreateFile(FileName,
                       GENERIC_READ,
                       FILE_SHARE_READ,
                       NULL,
                       OPEN_EXISTING,
                       FILE_ATTRIBUTE_NORMAL,
                       NULL);
            if (hFile == INVALID_HANDLE_VALUE) 
            {
              StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                               TEXT("CreateFile failed: %lx.\n"), 
                               GetLastError());
              MessageBox(hWnd, szMsg, TEXT("CreateFile"), MB_OK);
            }
        }
        return TRUE;

      case DBT_DEVICEREMOVEPENDING:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
          
            // The device is being removed;
            // close any open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      case DBT_DEVICEREMOVECOMPLETE:
        pDBHdr = (PDEV_BROADCAST_HDR) lParam;
        switch (pDBHdr->dbch_devicetype)
        {
          case DBT_DEVTYP_HANDLE:
            pDBHandle = (PDEV_BROADCAST_HANDLE) pDBHdr;
            // The device has been removed from the system;
            // unregister its notification handle

            UnregisterDeviceNotification(
              pDBHandle->dbch_hdevnotify);
              
            // The device has been removed;
            // close any remaining open handles to the file or device

            if (hFile != INVALID_HANDLE_VALUE) 
            {
              CloseHandle(hFile);
              hFile = INVALID_HANDLE_VALUE;
            }

        }
        return TRUE;

      default:
        return TRUE;
    }
  }
  default:
    return TRUE;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di evento del dispositivo](device-event-types.md)
</dt> </dl>

 

 



