---
description: Windows invia a tutte le finestre di primo livello un set di \_ messaggi WM DEVICECHANGE predefiniti quando vengono aggiunti nuovi dispositivi o supporti, ad esempio un CD o un DVD, che diventano disponibili e quando vengono rimossi i dispositivi o i supporti esistenti.
ms.assetid: 26baa3aa-e54d-42fe-b2b2-a3fcca6dee91
title: Rilevamento dell'inserimento o della rimozione dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6cfd4539d6f2ce5eac41e355f56a5a87835505
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132170"
---
# <a name="detecting-media-insertion-or-removal"></a>Rilevamento dell'inserimento o della rimozione dei supporti

Windows invia a tutte le finestre di primo livello un set di messaggi [**WM \_ DEVICECHANGE**](wm-devicechange.md) predefiniti quando vengono aggiunti nuovi dispositivi o supporti, ad esempio un CD o un DVD, che diventano disponibili e quando vengono rimossi i dispositivi o i supporti esistenti. Non è necessario eseguire la registrazione per ricevere questi messaggi predefiniti. Vedere la sezione Osservazioni in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) per informazioni dettagliate sui messaggi inviati per impostazione predefinita. I messaggi nell'esempio di codice seguente sono tra i messaggi predefiniti.

> [!Note]  
> Windows invia solo i messaggi [**WM \_ DEVICECHANGE**](wm-devicechange.md) per gli eventi multimediali di CD o DVD alle finestre di primo livello di proprietà delle applicazioni eseguite nella sessione della console attiva. Le finestre di primo livello di proprietà delle applicazioni eseguite in una sessione Desktop remoto non ricevono messaggi [**WM \_ DEVICECHANGE**](wm-devicechange.md) per eventi multimediali CD o DVD.

 

A ogni messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) è associato un evento che descrive la modifica e una struttura che fornisce informazioni dettagliate sulla modifica. La struttura è costituita da un'intestazione indipendente dall'evento, [**dev \_ broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), seguita da membri dipendenti dall'evento. I membri dipendenti dall'evento descrivono il dispositivo a cui si applica l'evento. Per usare questa struttura, le applicazioni devono innanzitutto determinare il tipo di evento e il tipo di dispositivo. Quindi, possono utilizzare la struttura corretta per eseguire l'azione appropriata.

Quando l'utente inserisce un nuovo CD o DVD in un'unità, le applicazioni ricevono un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con un evento [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) . L'applicazione deve controllare l'evento per verificare che il tipo di dispositivo in arrivo sia un volume (il membro **dbch \_ DeviceType** è **DBT \_ DEVTYP \_ volume**) e che la modifica influisca sul supporto (il membro dei **\_ flag dbcv** è un **\_ supporto DBTF**).

Quando l'utente rimuove un CD o un DVD da un'unità, le applicazioni ricevono un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con un evento [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) . Anche in questo caso, l'applicazione deve controllare l'evento per verificare che il dispositivo rimosso sia un volume e che la modifica influisca sul supporto.

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

[Eventi dispositivo](device-events.md)
</dt> </dl>

 

 



