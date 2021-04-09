---
description: I provider di pacchetti di rete (centrali) sono Network Monitor componenti di sistema che raccolgono il traffico di rete (frame) dalla rete e li passano all'interfaccia utente Network Monitor e alle applicazioni NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Provider di pacchetti di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885469"
---
# <a name="network-packet-providers"></a><span data-ttu-id="5f249-103">Provider di pacchetti di rete</span><span class="sxs-lookup"><span data-stu-id="5f249-103">Network Packet Providers</span></span>

<span data-ttu-id="5f249-104">I provider di pacchetti di rete (centrali) sono Network Monitor componenti di sistema che raccolgono il traffico di rete (frame) dalla rete e li passano all'interfaccia utente Network Monitor e alle [*applicazioni NPP*](n.md).</span><span class="sxs-lookup"><span data-stu-id="5f249-104">Network packet providers (NPPs) are Network Monitor system components that collect network traffic (frames) from the network and pass them on to the Network Monitor UI, and [*NPP applications*](n.md).</span></span>

<span data-ttu-id="5f249-105">Nella figura seguente vengono illustrati due centrali: la NPP di NDIS fornita da Network Monitor e un NPP personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5f249-105">The following illustration shows two NPPs: the NDIS NPP provided by Network Monitor and a custom NPP.</span></span>

![NPP di NDIS fornito da Network Monitor e da un NPP personalizzato](images/npp.png)

<span data-ttu-id="5f249-107">Viene Ndisnpp.dll la NPP di NDIS fornita da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="5f249-107">The NDIS NPP provided by Network Monitor is Ndisnpp.dll.</span></span> <span data-ttu-id="5f249-108">Questo NPP usa il driver di sistema Network Monitor (Nmnt.sys) per ottenere i frame raccolti dalla rete e diverse interfacce COM (definite interfacce NPP) per passare i frame all'interfaccia utente Network Monitor e le applicazioni NPP, dove possono essere visualizzate e analizzate.</span><span class="sxs-lookup"><span data-stu-id="5f249-108">This NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network and several COM interfaces (referred to as the NPP interfaces) to pass the frames on to the Network Monitor UI, and NPP applications, where they can be displayed and analyzed.</span></span>

<span data-ttu-id="5f249-109">Ndisnpp.dll si connette al livello [*NDIS*](n.md) per ottenere il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="5f249-109">Ndisnpp.dll connects to the [*NDIS*](n.md) layer to obtain its network traffic.</span></span> <span data-ttu-id="5f249-110">(Centrali personalizzato può ignorare il livello NDIS e comunicare direttamente con l'hardware di rete). Tenere presente che, indipendentemente dal fatto che un NPP usi NDIS, centrali può connettersi a un numero qualsiasi di schede di rete e tutti i centrali devono supportare le stesse interfacce NPP.</span><span class="sxs-lookup"><span data-stu-id="5f249-110">(Custom NPPs can bypass the NDIS layer and communicate directly with the networking hardware.) Be aware that regardless of whether an NPP uses NDIS, NPPs can connect to any number of network cards and that all NPPs must support the same NPP interfaces.</span></span>

<span data-ttu-id="5f249-111">Prima che un'applicazione possa iniziare a acquisire i dati, è necessario:</span><span class="sxs-lookup"><span data-stu-id="5f249-111">Before an application can start to capture data, it must:</span></span>

-   <span data-ttu-id="5f249-112">Selezionare la scheda di interfaccia di rete (NIC) che collegherà l'NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="5f249-112">Select the network interface card (NIC) that will connect the NPP to the network.</span></span>
-   <span data-ttu-id="5f249-113">Selezionare l'interfaccia NPP che verrà usata per acquisire i frame di rete.</span><span class="sxs-lookup"><span data-stu-id="5f249-113">Select the NPP interface that will be used to capture the network frames.</span></span>
-   <span data-ttu-id="5f249-114">Usare l'interfaccia selezionata per connettersi alla scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="5f249-114">Use the selected interface to connect to the NIC.</span></span>

<span data-ttu-id="5f249-115">Per ulteriori informazioni su come enumerare e selezionare una scheda di interfaccia di rete, vedere [selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md).</span><span class="sxs-lookup"><span data-stu-id="5f249-115">For more information about how to enumerate and select a network interface card, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md).</span></span>

<span data-ttu-id="5f249-116">Per ulteriori informazioni sulle interfacce COM esposte da centrali, vedere [selezione di un'interfaccia NPP](selecting-an-npp-interface.md).</span><span class="sxs-lookup"><span data-stu-id="5f249-116">For more information about COM interfaces exposed by NPPs, see [Selecting an NPP Interface](selecting-an-npp-interface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f249-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f249-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f249-118">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="5f249-118">**IDelaydC**</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="5f249-119">**IESP**</span><span class="sxs-lookup"><span data-stu-id="5f249-119">**IESP**</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="5f249-120">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="5f249-120">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="5f249-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="5f249-121">**IStats**</span></span>](istats.md)
</dt> </dl>

 

 



