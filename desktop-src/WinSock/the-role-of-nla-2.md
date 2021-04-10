---
description: Il provider di servizi di riconoscimento del percorso di rete è essenziale per i computer o i dispositivi che possono spostarsi tra reti diverse e per selezionare configurazioni ottimali quando sono disponibili più di uno.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Ruolo di NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226957"
---
# <a name="the-role-of-nla"></a><span data-ttu-id="b5991-103">Ruolo di NLA</span><span class="sxs-lookup"><span data-stu-id="b5991-103">The Role of NLA</span></span>

<span data-ttu-id="b5991-104">Il provider di servizi di riconoscimento del percorso di rete è essenziale per i computer o i dispositivi che possono spostarsi tra reti diverse e per selezionare configurazioni ottimali quando sono disponibili più di uno.</span><span class="sxs-lookup"><span data-stu-id="b5991-104">The Network Location Awareness (NLA) service provider is vital for computers or devices that might move between different networks, and for selecting optimal configurations when more than one is available.</span></span> <span data-ttu-id="b5991-105">Ad esempio, un computer wireless che effettua il roaming tra reti fisiche può utilizzare NLA per determinare la configurazione corretta in base alle informazioni sulla connessione di rete disponibile.</span><span class="sxs-lookup"><span data-stu-id="b5991-105">For example, a wireless computer roaming between physical networks can use NLA to determine the proper configuration based on information about its available network connection.</span></span> <span data-ttu-id="b5991-106">NLA si rivela utile anche quando un computer multihomed dispone di una connessione fisica a una rete, mentre è connessa anche a un'altra rete tramite una connessione remota o un tunnel.</span><span class="sxs-lookup"><span data-stu-id="b5991-106">NLA also proves valuable when a multihomed computer has a physical connection to one network while also connected to another network through a dial-up connection or a tunnel.</span></span>

<span data-ttu-id="b5991-107">In passato, gli sviluppatori dovevano ottenere informazioni su un'interfaccia di rete logica e quindi prendere decisioni sulla connettività di rete, in base a una grande quantità di informazioni di rete diversi.</span><span class="sxs-lookup"><span data-stu-id="b5991-107">In the past, developers had to obtain information about a logical network interface, and therefore make decisions about network connectivity, based on a multitude of disparate network information.</span></span> <span data-ttu-id="b5991-108">In questi casi, gli sviluppatori devono scegliere l'interfaccia di rete appropriata in base all'indirizzo IP, alla subnet dell'interfaccia, al nome del Domain Name System (DNS) associato all'interfaccia, all'indirizzo MAC di una scheda di interfaccia di rete, a un nome di rete wireless o ad altre informazioni sulla rete.</span><span class="sxs-lookup"><span data-stu-id="b5991-108">In those circumstances, developers had to choose the appropriate network interface based on the IP address, the subnet of the interface, the Domain Name System (DNS) name associated with the interface, the MAC address of a NIC, a wireless network name, or other network information.</span></span> <span data-ttu-id="b5991-109">NLA attenua questo problema fornendo un'interfaccia standard per l'enumerazione delle informazioni sugli allegati di rete logica, la correlazione con le informazioni sull'interfaccia di rete fisica e quindi la notifica quando le informazioni restituite in precedenza vengono invalidate.</span><span class="sxs-lookup"><span data-stu-id="b5991-109">NLA alleviates this problem by supplying a standard interface for enumerating logical network attachment information, correlating it with physical network interface information, and then providing notification when previously returned information gets invalidated.</span></span>

<span data-ttu-id="b5991-110">NLA fornisce le seguenti informazioni sul percorso di rete:</span><span class="sxs-lookup"><span data-stu-id="b5991-110">NLA provides the following network location information:</span></span>

<dl> <dt>

<span data-ttu-id="b5991-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identità rete logica</span><span class="sxs-lookup"><span data-stu-id="b5991-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Logical Network Identity</span></span>
</dt> <dd>

<span data-ttu-id="b5991-112">NLA tenta innanzitutto di identificare una rete logica in base al nome di dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="b5991-112">NLA first attempts to identify a logical network by its DNS domain name.</span></span> <span data-ttu-id="b5991-113">Se una rete logica non ha un nome di dominio, NLA identifica la rete da informazioni statiche personalizzate archiviate nel registro di sistema e infine dall'indirizzo della subnet.</span><span class="sxs-lookup"><span data-stu-id="b5991-113">If a logical network does not have a domain name, NLA identifies the network from custom static information stored in the registry, and finally from its subnet address.</span></span>

</dd> <dt>

<span data-ttu-id="b5991-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfacce di rete logiche</span><span class="sxs-lookup"><span data-stu-id="b5991-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logical Network Interfaces</span></span>
</dt> <dd>

<span data-ttu-id="b5991-115">Per ogni rete a cui è collegato un computer, NLA fornisce un *AdapterName* che identifica in modo univoco un'interfaccia fisica, ad esempio una NIC, oppure un'interfaccia logica quale una connessione RAS.</span><span class="sxs-lookup"><span data-stu-id="b5991-115">For each network to which a computer is attached, NLA supplies an *AdapterName* that uniquely identifies a physical interface such as a NIC, or a logical interface such as a RAS connection.</span></span> <span data-ttu-id="b5991-116">AdapterName può quindi essere usato con le funzioni disponibili nell'API helper IP per ottenere ulteriori caratteristiche di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b5991-116">The AdapterName can then be used with functions available in the IP Helper API to obtain further interface characteristics.</span></span>

</dd> </dl>

<span data-ttu-id="b5991-117">NLA implementa la rete logica come classe del servizio, con le proprietà e il GUID della classe associati.</span><span class="sxs-lookup"><span data-stu-id="b5991-117">NLA implements the logical network as a service class, with an associated class GUID and properties.</span></span> <span data-ttu-id="b5991-118">Ogni rete logica per cui NLA restituisce informazioni è un'istanza di tale classe di servizio.</span><span class="sxs-lookup"><span data-stu-id="b5991-118">Each logical network for which NLA returns information is an instance of that service class.</span></span>

 

 



