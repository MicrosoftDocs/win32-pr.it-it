---
title: Application Layer Enforcement (ALE)
description: ALE è un set di livelli in modalità kernel di Windows Filtering Platform (WFP) usati per il filtro con stato.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398977"
---
# <a name="application-layer-enforcement-ale"></a><span data-ttu-id="07cf0-103">Application Layer Enforcement (ALE)</span><span class="sxs-lookup"><span data-stu-id="07cf0-103">Application Layer Enforcement (ALE)</span></span>

<span data-ttu-id="07cf0-104">ALE è un set di livelli in modalità kernel di Windows Filtering Platform (WFP) usati per il filtro con stato.</span><span class="sxs-lookup"><span data-stu-id="07cf0-104">ALE is a set of Windows Filtering Platform (WFP) kernel-mode layers that are used for stateful filtering.</span></span>

<span data-ttu-id="07cf0-105">Il filtro con stato tiene traccia dello stato delle connessioni di rete e consente solo i pacchetti che corrispondono a uno stato di connessione noto.</span><span class="sxs-lookup"><span data-stu-id="07cf0-105">Stateful filtering keeps track of the state of network connections and allows only packets that match a known connection state.</span></span> <span data-ttu-id="07cf0-106">Ad esempio, il filtro con stato per una connessione TCP avviata da un firewall può consentire solo i pacchetti in ingresso che corrispondono ai pacchetti in uscita precedenti inviati dall'entità protetta.</span><span class="sxs-lookup"><span data-stu-id="07cf0-106">For example, stateful filtering for a TCP connection initiated from behind a firewall can allow only incoming packets that match previous outgoing packets sent by the party protected.</span></span>

<span data-ttu-id="07cf0-107">I filtri nei livelli ALE autorizzano la creazione di connessioni in ingresso e in uscita, le assegnazioni delle porte, le operazioni socket come [**Listen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), la creazione di socket non elaborati e la ricezione in modalità promiscua.</span><span class="sxs-lookup"><span data-stu-id="07cf0-107">Filters in the ALE layers authorize inbound and outbound connection creation, port assignments, socket operations such as [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen), raw socket creation, and promiscuous mode receiving.</span></span>

<span data-ttu-id="07cf0-108">Il traffico ai livelli ALE è classificato come operazione per connessione o per socket.</span><span class="sxs-lookup"><span data-stu-id="07cf0-108">Traffic at the ALE layers is classified either per-connection or per-socket operation.</span></span> <span data-ttu-id="07cf0-109">Ai livelli non ALE i filtri possono solo classificare il traffico in base ai singoli pacchetti.</span><span class="sxs-lookup"><span data-stu-id="07cf0-109">At non-ALE layers, filters can only classify traffic on a per-packet basis.</span></span>

<span data-ttu-id="07cf0-110">I livelli ALE sono gli unici livelli PAM in cui è possibile filtrare il traffico di rete in base all'identità dell'applicazione, usando un nome di file normalizzato, e in base all'identità dell'utente, usando un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="07cf0-110">ALE layers are the only WFP layers where network traffic can be filtered based on the application identity—using a normalized file name—and based on the user identity—using a security descriptor.</span></span> <span data-ttu-id="07cf0-111">(Vedere FLT \_ \_ \_ Informazioni sul nome file nella documentazione di Windows Driver Kit (WDK), per ulteriori informazioni sui nomi file normalizzati.</span><span class="sxs-lookup"><span data-stu-id="07cf0-111">(See FLT\_FILE\_NAME\_INFORMATION in the Windows Driver Kit (WDK) documentation, for more information on normalized file names.)</span></span>

<span data-ttu-id="07cf0-112">Inoltre, quando si usa IPsec per proteggere la connessione, è possibile eseguire il filtro ai livelli ALE anche sull'identità del computer remoto e sull'identità utente remota.</span><span class="sxs-lookup"><span data-stu-id="07cf0-112">In addition, when IPsec is used to secure the connection, filtering at ALE layers can also be performed on the remote machine identity and on the remote user identity.</span></span> <span data-ttu-id="07cf0-113">Le identità del computer remoto e dell'utente vengono ottenute dalle credenziali utilizzate per la creazione di una sessione IPsec.</span><span class="sxs-lookup"><span data-stu-id="07cf0-113">The remote machine and user identities are obtained from the credentials used in the creation of an IPsec session.</span></span>

<span data-ttu-id="07cf0-114">Per questo motivo, i criteri che impongono chi (ad esempio, "amministratore") e/o quale applicazione (ad esempio, "Internet Explorer") sono autorizzati a eseguire le operazioni di rete citate sopra vengono creati a livello di ALE.</span><span class="sxs-lookup"><span data-stu-id="07cf0-114">For this reason, policies that enforce who (for example, "administrator") and/or which application (for example, "Internet Explorer") are allowed to perform the network operations mentioned above are authored at the ALE layers.</span></span>

<span data-ttu-id="07cf0-115">ALE fornisce l'imposizione dei criteri, ad esempio "Consenti a Windows Messenger di accedere alla rete durante il blocco di tutte le altre applicazioni".</span><span class="sxs-lookup"><span data-stu-id="07cf0-115">ALE provides enforcement for policies such as "allow Windows Messenger all access to the network while blocking all other applications."</span></span> <span data-ttu-id="07cf0-116">In questo esempio, quando l'applicazione "Messenger" si connette attraverso la rete, ALE intercetta l'evento, determina che è stato avviato da Messenger ed esegue una query sul motore di filtro WFP per determinare se il socket deve essere autorizzato a continuare.</span><span class="sxs-lookup"><span data-stu-id="07cf0-116">In such an example, when the application "Messenger" connects across the network, ALE traps the event, determines that it was initiated by Messenger and queries the WFP filter engine to determine whether the socket should be allowed to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="07cf0-117">A causa della natura dei socket dual-IP reali, le classificazioni a livello di ALE IPv4 potrebbero non verificarsi.</span><span class="sxs-lookup"><span data-stu-id="07cf0-117">Due to the nature of true dual-IP sockets, classifications at the IPv4 ALE layer may not occur.</span></span> <span data-ttu-id="07cf0-118">Questo è dovuto alla progettazione, perché per tutti gli Intent e gli scopi, il socket è un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="07cf0-118">This is by design, because for all intents and purposes, the socket is an IPv6 socket.</span></span> <span data-ttu-id="07cf0-119">Per visualizzare il traffico V4 per un socket di questo tipo, creare filtri a livello V6 usando l'indirizzo mappato a IPv6.</span><span class="sxs-lookup"><span data-stu-id="07cf0-119">To see the V4 traffic for such a socket, create filters at the V6 layer using the IPv6-mapped address.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="07cf0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07cf0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07cf0-121">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="07cf0-121">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="07cf0-122">Filtro con stato ALE</span><span class="sxs-lookup"><span data-stu-id="07cf0-122">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="07cf0-123">Traffico di broadcast/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="07cf0-123">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="07cf0-124">Riautorizzazione ALE</span><span class="sxs-lookup"><span data-stu-id="07cf0-124">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="07cf0-125">Personalizzazione del flusso di ALE</span><span class="sxs-lookup"><span data-stu-id="07cf0-125">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 