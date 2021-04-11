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
# <a name="detecting-media-insertion-or-removal"></a><span data-ttu-id="c9d73-103">Rilevamento dell'inserimento o della rimozione dei supporti</span><span class="sxs-lookup"><span data-stu-id="c9d73-103">Detecting Media Insertion or Removal</span></span>

<span data-ttu-id="c9d73-104">Windows invia a tutte le finestre di primo livello un set di messaggi [**WM \_ DEVICECHANGE**](wm-devicechange.md) predefiniti quando vengono aggiunti nuovi dispositivi o supporti, ad esempio un CD o un DVD, che diventano disponibili e quando vengono rimossi i dispositivi o i supporti esistenti.</span><span class="sxs-lookup"><span data-stu-id="c9d73-104">Windows sends all top-level windows a set of default [**WM\_DEVICECHANGE**](wm-devicechange.md) messages when new devices or media (such as a CD or DVD) are added and become available, and when existing devices or media are removed.</span></span> <span data-ttu-id="c9d73-105">Non è necessario eseguire la registrazione per ricevere questi messaggi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c9d73-105">You do not need to register to receive these default messages.</span></span> <span data-ttu-id="c9d73-106">Vedere la sezione Osservazioni in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) per informazioni dettagliate sui messaggi inviati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c9d73-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details on which messages are sent by default.</span></span> <span data-ttu-id="c9d73-107">I messaggi nell'esempio di codice seguente sono tra i messaggi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c9d73-107">The messages in the code example below are among the default messages.</span></span>

> [!Note]  
> <span data-ttu-id="c9d73-108">Windows invia solo i messaggi [**WM \_ DEVICECHANGE**](wm-devicechange.md) per gli eventi multimediali di CD o DVD alle finestre di primo livello di proprietà delle applicazioni eseguite nella sessione della console attiva.</span><span class="sxs-lookup"><span data-stu-id="c9d73-108">Windows only sends [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events to top-level windows that are owned by applications that run in the active console session.</span></span> <span data-ttu-id="c9d73-109">Le finestre di primo livello di proprietà delle applicazioni eseguite in una sessione Desktop remoto non ricevono messaggi [**WM \_ DEVICECHANGE**](wm-devicechange.md) per eventi multimediali CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="c9d73-109">Top-level windows that are owned by applications that run in a remote desktop session do not receive [**WM\_DEVICECHANGE**](wm-devicechange.md) messages for CD or DVD media events.</span></span>

 

<span data-ttu-id="c9d73-110">A ogni messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) è associato un evento che descrive la modifica e una struttura che fornisce informazioni dettagliate sulla modifica.</span><span class="sxs-lookup"><span data-stu-id="c9d73-110">Each [**WM\_DEVICECHANGE**](wm-devicechange.md) message has an associated event that describes the change, and a structure that provides detailed information about the change.</span></span> <span data-ttu-id="c9d73-111">La struttura è costituita da un'intestazione indipendente dall'evento, [**dev \_ broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), seguita da membri dipendenti dall'evento.</span><span class="sxs-lookup"><span data-stu-id="c9d73-111">The structure consists of an event-independent header, [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr), followed by event-dependent members.</span></span> <span data-ttu-id="c9d73-112">I membri dipendenti dall'evento descrivono il dispositivo a cui si applica l'evento.</span><span class="sxs-lookup"><span data-stu-id="c9d73-112">The event-dependent members describe the device to which the event applies.</span></span> <span data-ttu-id="c9d73-113">Per usare questa struttura, le applicazioni devono innanzitutto determinare il tipo di evento e il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9d73-113">To use this structure, applications must first determine the event type and the device type.</span></span> <span data-ttu-id="c9d73-114">Quindi, possono utilizzare la struttura corretta per eseguire l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="c9d73-114">Then, they can use the correct structure to take appropriate action.</span></span>

<span data-ttu-id="c9d73-115">Quando l'utente inserisce un nuovo CD o DVD in un'unità, le applicazioni ricevono un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con un evento [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d73-115">When the user inserts a new CD or DVD into a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEARRIVAL](dbt-devicearrival.md) event.</span></span> <span data-ttu-id="c9d73-116">L'applicazione deve controllare l'evento per verificare che il tipo di dispositivo in arrivo sia un volume (il membro **dbch \_ DeviceType** è **DBT \_ DEVTYP \_ volume**) e che la modifica influisca sul supporto (il membro dei **\_ flag dbcv** è un **\_ supporto DBTF**).</span><span class="sxs-lookup"><span data-stu-id="c9d73-116">The application must check the event to ensure that the type of device arriving is a volume (the **dbch\_devicetype** member is **DBT\_DEVTYP\_VOLUME**) and that the change affects the media (the **dbcv\_flags** member is **DBTF\_MEDIA**).</span></span>

<span data-ttu-id="c9d73-117">Quando l'utente rimuove un CD o un DVD da un'unità, le applicazioni ricevono un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con un evento [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d73-117">When the user removes a CD or DVD from a drive, applications receive a [**WM\_DEVICECHANGE**](wm-devicechange.md) message with a [DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) event.</span></span> <span data-ttu-id="c9d73-118">Anche in questo caso, l'applicazione deve controllare l'evento per verificare che il dispositivo rimosso sia un volume e che la modifica influisca sul supporto.</span><span class="sxs-lookup"><span data-stu-id="c9d73-118">Again, the application must check the event to ensure that the device being removed is a volume and that the change affects the media.</span></span>

<span data-ttu-id="c9d73-119">Il codice seguente illustra come verificare l'inserimento o la rimozione di un CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="c9d73-119">The following code demonstrates how to check for insertion or removal of a CD or DVD.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c9d73-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9d73-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d73-121">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="c9d73-121">Device Events</span></span>](device-events.md)
</dt> </dl>

 

 



