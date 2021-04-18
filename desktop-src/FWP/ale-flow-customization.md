---
title: Personalizzazione del flusso di ALE
description: È possibile personalizzare il filtro di rete a livello di applicazione dei livelli di applicazione (ALE) di Windows Filtering Platform (PAM) aggiungendo filtri con opzioni di classificazione specifiche.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104336450"
---
# <a name="ale-flow-customization"></a><span data-ttu-id="41c79-103">Personalizzazione del flusso di ALE</span><span class="sxs-lookup"><span data-stu-id="41c79-103">ALE Flow Customization</span></span>

<span data-ttu-id="41c79-104">È possibile personalizzare il filtro di rete a livello di applicazione dei livelli di applicazione (ALE) di Windows Filtering Platform (PAM) aggiungendo filtri con opzioni di classificazione specifiche.</span><span class="sxs-lookup"><span data-stu-id="41c79-104">Network filtering at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) can be customized by adding filters with specific classify options.</span></span>

## <a name="multicastbroadcast-traffic"></a><span data-ttu-id="41c79-105">Traffico multicast/broadcast</span><span class="sxs-lookup"><span data-stu-id="41c79-105">Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="41c79-106">Per bloccare il traffico in ingresso in base a stati broadcast o multicast in uscita, aggiungere un filtro che autorizza il multicast in uscita e il traffico broadcast e con l'opzione [**FWP \_ classificate \_ option \_ multicast \_ state**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) impostata sul **\_ valore FWP opzione \_ \_ Deny \_ multicast \_ state**.</span><span class="sxs-lookup"><span data-stu-id="41c79-106">To block inbound traffic based on outbound multicast or broadcast states, add a filter that authorizes outbound multicast and broadcast traffic and that has the [**FWP\_CLASSIFY\_OPTION\_MULTICAST\_STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_DENY\_MULTICAST\_STATE**.</span></span>

## <a name="remote-peers"></a><span data-ttu-id="41c79-107">Peer remoti</span><span class="sxs-lookup"><span data-stu-id="41c79-107">Remote Peers</span></span>

<span data-ttu-id="41c79-108">Per aggiungere pacchetti di risposta da peer diversi allo stesso flusso di ALE, aggiungere un filtro con l'opzione [**FWP \_ classificate \_ \_ Loose \_ source \_ mapping**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) opzione impostata su **FWP \_ opzione \_ \_ Abilita il \_ \_ \_ mapping del codice sorgente libero**.</span><span class="sxs-lookup"><span data-stu-id="41c79-108">To add response packets from different peers to the same ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_LOOSE\_SOURCE\_MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_ENABLE\_LOOSE\_SOURCE\_MAPPING**.</span></span>

<span data-ttu-id="41c79-109">Per un esempio di codice, vedere [utilizzo delle opzioni classifica](using-classify-options.md) .</span><span class="sxs-lookup"><span data-stu-id="41c79-109">See [Using Classify Options](using-classify-options.md) for code sample.</span></span>

## <a name="ale-flow-lifetime"></a><span data-ttu-id="41c79-110">Durata del flusso ALE</span><span class="sxs-lookup"><span data-stu-id="41c79-110">ALE Flow Lifetime</span></span>

<span data-ttu-id="41c79-111">Per modificare i valori di timeout di inattività per un flusso di ALE, aggiungere un filtro con l'opzione [**FWP \_ classificate option \_ \_ mcast \_ gettati \_ durata**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) e/o l'opzione di **\_ classificazione \_ \_ unicast \_ per la durata dell'opzione FWP classificate** sul valore di timeout di inattività desiderato.</span><span class="sxs-lookup"><span data-stu-id="41c79-111">To modify the idle timeout values for an ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_MCAST\_BCAST\_LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option and/or the **FWP\_CLASSIFY\_OPTION\_UNICAST\_LIFETIME** option set to the desired idle timeout value.</span></span>

<span data-ttu-id="41c79-112">Vedere [uso delle opzioni di classificazione](using-classify-options.md) per un esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="41c79-112">See [Using Classify Options](using-classify-options.md) for a code sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41c79-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41c79-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41c79-114">Application Layer Enforcement (ALE)</span><span class="sxs-lookup"><span data-stu-id="41c79-114">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="41c79-115">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="41c79-115">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="41c79-116">Filtro con stato ALE</span><span class="sxs-lookup"><span data-stu-id="41c79-116">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="41c79-117">Traffico di broadcast/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="41c79-117">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="41c79-118">Riautorizzazione ALE</span><span class="sxs-lookup"><span data-stu-id="41c79-118">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="41c79-119">Uso delle opzioni di classificazione</span><span class="sxs-lookup"><span data-stu-id="41c79-119">Using Classify Options</span></span>](using-classify-options.md)
</dt> </dl>

 

 




