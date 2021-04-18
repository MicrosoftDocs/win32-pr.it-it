---
description: Modifiche al formato dinamico
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Modifiche al formato dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304009"
---
# <a name="dynamic-format-changes"></a><span data-ttu-id="17ba4-103">Modifiche al formato dinamico</span><span class="sxs-lookup"><span data-stu-id="17ba4-103">Dynamic Format Changes</span></span>

<span data-ttu-id="17ba4-104">Quando due filtri si connettono, accettano un tipo di supporto che descrive il formato dei dati che verranno recapitati dal filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="17ba4-104">When two filters connect, they agree on a media type, which describes the format of the data that the upstream filter will deliver.</span></span> <span data-ttu-id="17ba4-105">Nella maggior parte dei casi, il tipo di supporto è fisso per la durata della connessione.</span><span class="sxs-lookup"><span data-stu-id="17ba4-105">In most cases, the media type is fixed for the duration of the connection.</span></span> <span data-ttu-id="17ba4-106">Tuttavia, DirectShow offre un supporto limitato per i filtri per modificare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="17ba4-106">However, DirectShow does offer limited support for filters to change the media type.</span></span> <span data-ttu-id="17ba4-107">Quando un filtro cambia i tipi di supporto, viene chiamato *modifica del formato dinamico*.</span><span class="sxs-lookup"><span data-stu-id="17ba4-107">When a filter switches media types, it is called a *dynamic format change*.</span></span> <span data-ttu-id="17ba4-108">Se si sta scrivendo un filtro DirectShow, è necessario essere a conoscenza dei meccanismi per le modifiche del formato dinamico.</span><span class="sxs-lookup"><span data-stu-id="17ba4-108">If you are writing a DirectShow filter, you should be aware of the mechanisms for dynamic format changes.</span></span> <span data-ttu-id="17ba4-109">Anche se il filtro non supporta tali modifiche, dovrebbe rispondere correttamente se un altro filtro richiede un nuovo formato.</span><span class="sxs-lookup"><span data-stu-id="17ba4-109">Even if your filter does not support such changes, it should respond correctly if another filter requests a new format.</span></span>

<span data-ttu-id="17ba4-110">DirectShow definisce diversi meccanismi distinti per le modifiche del formato dinamico, a seconda dello stato del grafico del filtro e del tipo di modifica richiesto.</span><span class="sxs-lookup"><span data-stu-id="17ba4-110">DirectShow defines several distinct mechanisms for dynamic format changes, depending on the state of filter graph and the type of change that is required.</span></span>

-   <span data-ttu-id="17ba4-111">Se il grafo viene arrestato, i pin possono riconnettersi e rinegoziare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="17ba4-111">If the graph is stopped, the pins can reconnect and renegotiate the media type.</span></span> <span data-ttu-id="17ba4-112">Per ulteriori informazioni, vedere [riconnessione dei pin](reconnecting-pins.md).</span><span class="sxs-lookup"><span data-stu-id="17ba4-112">For more information, see [Reconnecting Pins](reconnecting-pins.md).</span></span>
-   <span data-ttu-id="17ba4-113">Alcuni filtri possono riconnettere i pin anche quando il grafico è attivo (in esecuzione o in pausa).</span><span class="sxs-lookup"><span data-stu-id="17ba4-113">Some filters can reconnect pins even while the graph is active (running or paused).</span></span> <span data-ttu-id="17ba4-114">Per ulteriori informazioni su questo meccanismo, vedere [riconnessione dinamica](dynamic-reconnection.md).</span><span class="sxs-lookup"><span data-stu-id="17ba4-114">For more information about this mechanism, see [Dynamic Reconnection](dynamic-reconnection.md).</span></span>

<span data-ttu-id="17ba4-115">In caso contrario, se il grafico è attivo, ma i filtri in questione non supportano la riconnessione dinamica dei pin, esistono tre meccanismi possibili per modificare il formato:</span><span class="sxs-lookup"><span data-stu-id="17ba4-115">Otherwise, if the graph is active, but the filters in question do not support dynamic pin reconnections, there are three possible mechanisms for changing the format:</span></span>

-   <span data-ttu-id="17ba4-116">[QueryAccept (downstream)](queryaccept--downstream.md) viene usato quando un pin di output propone una modifica di formato al relativo peer downstream, ma solo se il nuovo formato non richiede un buffer più grande.</span><span class="sxs-lookup"><span data-stu-id="17ba4-116">[QueryAccept (Downstream)](queryaccept--downstream.md) is used when If an output pin proposes a format change to its downstream peer, but only if the new format does not require a larger buffer.</span></span>
-   <span data-ttu-id="17ba4-117">[QueryAccept (upstream)](queryaccept--upstream.md) viene usato quando un pin di input propone una modifica al formato del peer upstream.</span><span class="sxs-lookup"><span data-stu-id="17ba4-117">[QueryAccept (Upstream)](queryaccept--upstream.md) is used when an input pin proposes a format change to its upstream peer.</span></span> <span data-ttu-id="17ba4-118">Il nuovo formato può avere le stesse dimensioni oppure può essere più grande.</span><span class="sxs-lookup"><span data-stu-id="17ba4-118">The new format can be the same size, or it can be larger.</span></span>
-   <span data-ttu-id="17ba4-119">[ReceiveConnection](receiveconnection.md) viene usato quando un pin di output propone una modifica di formato al peer downstream e il nuovo formato richiede un buffer più grande.</span><span class="sxs-lookup"><span data-stu-id="17ba4-119">[ReceiveConnection](receiveconnection.md) is used when an output pin proposes a format change to its downstream peer, and the new format requires a larger buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17ba4-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17ba4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17ba4-121">Gestione delle modifiche al formato dal renderer video</span><span class="sxs-lookup"><span data-stu-id="17ba4-121">Handling Format Changes from the Video Renderer</span></span>](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



