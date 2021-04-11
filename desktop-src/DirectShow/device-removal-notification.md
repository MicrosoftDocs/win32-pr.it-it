---
description: Notifica di rimozione del dispositivo
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notifica di rimozione del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965867"
---
# <a name="device-removal-notification"></a><span data-ttu-id="03a63-103">Notifica di rimozione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="03a63-103">Device Removal Notification</span></span>

<span data-ttu-id="03a63-104">Se l'utente rimuove un Plug and Play dispositivo utilizzato dal grafo, il gestore del grafico dei filtri Invia un evento di [**\_ \_ perdita del dispositivo EC**](ec-device-lost.md) .</span><span class="sxs-lookup"><span data-stu-id="03a63-104">If the user removes a Plug and Play device that the graph was using, the filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event.</span></span> <span data-ttu-id="03a63-105">Se il dispositivo torna nuovamente disponibile, il gestore del grafico dei filtri Invia un altro evento di **\_ \_ perdita del dispositivo EC** .</span><span class="sxs-lookup"><span data-stu-id="03a63-105">If the device becomes available again, the filter graph manager posts another **EC\_DEVICE\_LOST** event.</span></span> <span data-ttu-id="03a63-106">Lo stato precedente del filtro di acquisizione, tuttavia, non è più valido.</span><span class="sxs-lookup"><span data-stu-id="03a63-106">However, the previous state of the capture filter is no longer valid.</span></span> <span data-ttu-id="03a63-107">L'applicazione deve ricompilare il grafo per usare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03a63-107">The application must rebuild the graph to use the device.</span></span>

<span data-ttu-id="03a63-108">DirectShow non invia alcun evento quando viene collegato un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03a63-108">DirectShow does not send any event when a new device is plugged in.</span></span> <span data-ttu-id="03a63-109">Per informazioni sul momento in cui è disponibile un nuovo dispositivo, l'applicazione può monitorare \_ i messaggi della finestra WM DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="03a63-109">To learn when a new device is available, the application can monitor WM\_DEVICECHANGE window messages.</span></span> <span data-ttu-id="03a63-110">Per ulteriori informazioni, vedere la sezione relativa alla gestione dei dispositivi nella documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="03a63-110">For more information, see "Device Management" in the Platform SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03a63-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03a63-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03a63-112">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="03a63-112">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



