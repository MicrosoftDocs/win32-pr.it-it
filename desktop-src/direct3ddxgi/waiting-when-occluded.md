---
description: Le app possono attendere un evento quando il rendering sullo schermo non è necessario, ovvero quando sono bloccati.
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: In attesa di un evento quando il rendering non è necessario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303670"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a><span data-ttu-id="e8b6c-103">In attesa di un evento quando il rendering non è necessario</span><span class="sxs-lookup"><span data-stu-id="e8b6c-103">Waiting on an event when rendering is unnecessary</span></span>

<span data-ttu-id="e8b6c-104">Le app possono attendere un evento quando il rendering sullo schermo non è necessario, ovvero quando sono bloccati.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-104">Apps can wait on an event when rendering to the screen is unnecessary (that is, while they are occluded).</span></span> <span data-ttu-id="e8b6c-105">Quando il Gestione finestre desktop (DWM) o un'app è bloccato, non è necessario eseguire il rendering e il sistema operativo può rimanere in uno stato di alimentazione inferiore per periodi di tempo più lunghi.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-105">When the Desktop Window Manager (DWM) or an app is occluded, no rendering is necessary and the operating system can stay in lower power states for longer periods of time.</span></span> <span data-ttu-id="e8b6c-106">Questo consente di risparmiare energia ed estendere la durata della batteria.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-106">This saves power and extends battery life.</span></span>

<span data-ttu-id="e8b6c-107">Un'app può attendere un evento nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e8b6c-107">An app can wait on an event when:</span></span>

-   <span data-ttu-id="e8b6c-108">Tutti i monitoraggi sono disattivati.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-108">All the monitors are off.</span></span>
-   <span data-ttu-id="e8b6c-109">La sessione in cui viene eseguita l'app è disconnessa.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-109">The session that the app runs in is disconnected.</span></span>
-   <span data-ttu-id="e8b6c-110">L'app viene eseguita a schermo intero esclusivamente in una singola configurazione di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-110">The app runs in full screen exclusively on a single monitor configuration.</span></span>
-   <span data-ttu-id="e8b6c-111">L'app viene eseguita su un desktop diverso rispetto al desktop attivo e non dispone dell'autorizzazione per eseguire il rendering sul desktop attivo.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-111">The app runs on a different desktop than the active desktop and does not have permission to render on the active desktop.</span></span>

<span data-ttu-id="e8b6c-112">Il sistema operativo attiva l'evento quando l'app è in grado di eseguire nuovamente il rendering.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-112">The operating system triggers the event when the app is able to render again.</span></span> <span data-ttu-id="e8b6c-113">L'evento non viene cancellato durante un aggiornamento del driver o la processi di rilevamento e ripristino del timeout (TDR), ma viene cancellato quando il nuovo adapter e i monitoraggi diventano attivi.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-113">The event is not cleared during a driver upgrade, or timeout detection and recovery (TDR) procession, however it is cleared when the new adapter and monitors become active.</span></span>

<span data-ttu-id="e8b6c-114">Se si vuole che l'app riceva una notifica sulle modifiche dello stato di occlusione, l'app deve registrarsi per tali modifiche.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-114">If you want your app to be notified about changes of occlusion status, the app must register for these changes.</span></span> <span data-ttu-id="e8b6c-115">Un'app può registrarsi per ricevere notifiche sulle modifiche dello stato di occlusione tramite un messaggio a una finestra o tramite la segnalazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-115">An app can register to be notified about changes of occlusion status through a message to a window or through event signaling.</span></span> <span data-ttu-id="e8b6c-116">Per eseguire la registrazione per ricevere messaggi di notifica a una finestra in merito alle modifiche dello stato di occlusione, un'app chiama il metodo [**IDXGIFactory2:: RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) .</span><span class="sxs-lookup"><span data-stu-id="e8b6c-116">To register to receive notification messages to a window about occlusion status changes, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) method.</span></span> <span data-ttu-id="e8b6c-117">Per eseguire la registrazione per ricevere la notifica delle modifiche dello stato di occlusione tramite segnalazione eventi, un'app chiama il metodo [**IDXGIFactory2:: RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) .</span><span class="sxs-lookup"><span data-stu-id="e8b6c-117">To register to receive notification of occlusion status changes via event signaling, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) method.</span></span> <span data-ttu-id="e8b6c-118">Entrambi i metodi restituiscono un puntatore a un valore di chiave che l'app può usare per annullare la registrazione della notifica.</span><span class="sxs-lookup"><span data-stu-id="e8b6c-118">Both methods return a pointer to a key value that the app can use to unregister the notification.</span></span> <span data-ttu-id="e8b6c-119">Per annullare la registrazione della notifica, l'app passa il valore della chiave al metodo [**IDXGIFactory2:: UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .</span><span class="sxs-lookup"><span data-stu-id="e8b6c-119">To unregister the notification, the app passes this key value to the [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8b6c-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8b6c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8b6c-121">Miglioramenti di DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="e8b6c-121">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



