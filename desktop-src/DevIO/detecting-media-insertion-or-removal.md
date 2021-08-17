---
description: Windows invia a tutte le finestre di primo livello un set di messaggi DEVICECHANGE WM predefiniti quando nuovi dispositivi o supporti (ad esempio un CD o DVD) vengono aggiunti e diventano disponibili e quando i dispositivi o i supporti esistenti vengono \_ rimossi.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Rilevamento dell'inserimento o della rimozione di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3f6d579ed654ae2d2f77d00f70b88dc1441d03bbce59c0f8cb39ca6800c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318351"
---
# <a name="detecting-media-insertion-or-removal"></a>Rilevamento dell'inserimento o della rimozione di supporti

Windows invia a tutte le finestre di primo livello un set di messaggi [**\_ DEVICECHANGE WM**](wm-devicechange.md) predefiniti quando nuovi dispositivi o supporti (ad esempio un CD o DVD) vengono aggiunti e diventano disponibili e quando i dispositivi o i supporti esistenti vengono rimossi. Non è necessario registrarsi per ricevere questi messaggi predefiniti. Per informazioni dettagliate sui messaggi inviati per impostazione predefinita, vedere la sezione Osservazioni in [**RegisterDeviceNotification.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) I messaggi nell'esempio di codice seguente sono tra i messaggi predefiniti.

> [!Note]  
> Windows invia solo messaggi [**\_ DEVICECHANGE WM**](wm-devicechange.md) per eventi multimediali CD o DVD alle finestre di primo livello di proprietà delle applicazioni eseguite nella sessione della console attiva. Le finestre di primo livello di proprietà delle applicazioni eseguite in una sessione desktop remoto non ricevono messaggi [**\_ DEVICECHANGE WM**](wm-devicechange.md) per eventi multimediali CD o DVD.

 

A [**ogni messaggio WM \_ DEVICECHANGE**](wm-devicechange.md) è associato un evento che descrive la modifica e una struttura che fornisce informazioni dettagliate sulla modifica. La struttura è costituita da un'intestazione indipendente dagli eventi, [**DEV \_ BROADCAST \_ HDR,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)seguita da membri dipendenti dall'evento. I membri dipendenti dall'evento descrivono il dispositivo a cui si applica l'evento. Per usare questa struttura, le applicazioni devono prima determinare il tipo di evento e il tipo di dispositivo. Possono quindi usare la struttura corretta per eseguire le azioni appropriate.

Quando l'utente inserisce un nuovo CD o DVD in un'unità, le applicazioni ricevono un messaggio [**\_ DEVICECHANGE WM**](wm-devicechange.md) con un evento [ \_ DBT DEVICEARRIVAL.](dbt-devicearrival.md) L'applicazione deve controllare l'evento per assicurarsi che il tipo di dispositivo in arrivo sia un volume (il membro **dbch \_ devicetype** è **DBT \_ DEVTYP \_ VOLUME**) e che la modifica influisca sul supporto (il membro **\_ flag dbcv** è **DBTF \_ MEDIA**).

Quando l'utente rimuove un CD o DVD da un'unità, le applicazioni ricevono un [**messaggio \_ DEVICECHANGE WM**](wm-devicechange.md) con un [evento \_ DBT DEVICEREMOVECOMPLETE.](dbt-deviceremovecomplete.md) Anche in questo caso, l'applicazione deve controllare l'evento per assicurarsi che il dispositivo rimosso sia un volume e che la modifica influisca sul supporto.

Il codice seguente illustra come verificare l'inserimento o la rimozione di un CD o DVD.


```C++
#include <windows.h>
#include <dbt.h>
#include <strsafe.h>
#pragma comment(lib, "user32.lib" )

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam );
char FirstDriveFromMask( ULONG unitmask );  //prototype

/*------------------------------------------------------------------
   Main_OnDeviceChange( hwnd, wParam, lParam )

   Description
      Handles WM_DEVICECHANGE messages sent to the application's
      top-level window.
--------------------------------------------------------------------*/

void Main_OnDeviceChange( HWND hwnd, WPARAM wParam, LPARAM lParam )
 {
  PDEV_BROADCAST_HDR lpdb = (PDEV_BROADCAST_HDR)lParam;
  TCHAR szMsg[80];

  switch(wParam )
   {
    case DBT_DEVICEARRIVAL:
      // Check whether a CD or DVD was inserted into a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media has arrived.\n"), 
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE"), MB_OK );
         }
       }
      break;

    case DBT_DEVICEREMOVECOMPLETE:
      // Check whether a CD or DVD was removed from a drive.
      if (lpdb -> dbch_devicetype == DBT_DEVTYP_VOLUME)
       {
        PDEV_BROADCAST_VOLUME lpdbv = (PDEV_BROADCAST_VOLUME)lpdb;

        if (lpdbv -> dbcv_flags & DBTF_MEDIA)
         {
          StringCchPrintf( szMsg, sizeof(szMsg)/sizeof(szMsg[0]), 
                           TEXT("Drive %c: Media was removed.\n" ),
                           FirstDriveFromMask(lpdbv ->dbcv_unitmask) );

          MessageBox( hwnd, szMsg, TEXT("WM_DEVICECHANGE" ), MB_OK );
         }
       }
      break;

    default:
      /*
        Process other WM_DEVICECHANGE notifications for other 
        devices or reasons.
      */ 
      ;
   }
}

/*------------------------------------------------------------------
   FirstDriveFromMask( unitmask )

   Description
     Finds the first valid drive letter from a mask of drive letters.
     The mask must be in the format bit 0 = A, bit 1 = B, bit 2 = C, 
     and so on. A valid drive letter is defined when the 
     corresponding bit is set to 1.

   Returns the first drive letter that was found.
--------------------------------------------------------------------*/

char FirstDriveFromMask( ULONG unitmask )
 {
  char i;

  for (i = 0; i < 26; ++i)
   {
    if (unitmask & 0x1)
      break;
    unitmask = unitmask >> 1;
   }

  return( i + 'A' );
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Eventi del dispositivo](device-events.md)
</dt> </dl>

 

 



