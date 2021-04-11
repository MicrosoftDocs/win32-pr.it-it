---
description: Un'applicazione riceve un \_ evento DBT DEVICEQUERYREMOVE Device quando una funzionalità del sistema ha deciso di rimuovere un dispositivo specificato.
ms.assetid: 66f6c9f4-93fa-4ee8-adf8-cde4e63f9fb7
title: Elaborazione di una richiesta di rimozione di un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f6f1089cae0e4c9db964e3877cac8f8f8d8da4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126780"
---
# <a name="processing-a-request-to-remove-a-device"></a>Elaborazione di una richiesta di rimozione di un dispositivo

Un'applicazione riceve un evento [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) Device quando una funzionalità del sistema ha deciso di rimuovere un dispositivo specificato. Quando l'applicazione riceve questo evento, deve determinare se usa il dispositivo specificato e Annulla o prepara la rimozione.

Nell'esempio seguente, un'applicazione mantiene un handle aperto, hFile, al file o al dispositivo rappresentato da FileName. L'applicazione registra per la notifica degli eventi del dispositivo sul dispositivo sottostante chiamando la funzione [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) , usando un filtro di notifica del tipo di **\_ \_ handle DBT DEVTYP** e specificando la variabile hFile nel membro dell' **\_ handle dbch** del filtro.

L'applicazione elabora l'evento [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) Device chiudendo l'handle di file aperto al dispositivo da rimuovere. Nel caso in cui la rimozione del dispositivo venga annullata, l'applicazione elabora l'evento [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) Device per riaprire l'handle per il dispositivo. Dopo che il dispositivo è stato rimosso dal sistema, l'applicazione elabora gli eventi del dispositivo [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) e [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) annullando la registrazione dell'handle di notifica per il dispositivo e chiudendo gli handle ancora aperti al dispositivo.


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

 

 



