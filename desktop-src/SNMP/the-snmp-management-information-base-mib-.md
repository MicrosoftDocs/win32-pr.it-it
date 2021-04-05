---
title: MIB (Management Information Base) SNMP
description: Un set di oggetti gestiti viene descritto da un MIB (Management Information Base). Un'applicazione console di gestione SNMP può modificare gli oggetti in un computer specifico se il servizio SNMP dispone di una DLL dell'agente di estensione che supporta il MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708827"
---
# <a name="the-snmp-management-information-base-mib"></a><span data-ttu-id="5d7f3-104">MIB (Management Information Base) SNMP</span><span class="sxs-lookup"><span data-stu-id="5d7f3-104">The SNMP Management Information Base (MIB)</span></span>

<span data-ttu-id="5d7f3-105">Un set di oggetti gestiti viene descritto da un MIB (Management Information Base).</span><span class="sxs-lookup"><span data-stu-id="5d7f3-105">A Management Information Base (MIB) describes a set of managed objects.</span></span> <span data-ttu-id="5d7f3-106">Un'applicazione console di gestione SNMP può modificare gli oggetti in un computer specifico se il servizio SNMP dispone di una DLL dell'agente di estensione che supporta il MIB.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-106">An SNMP management console application can manipulate the objects on a specific computer if the SNMP service has an extension agent DLL that supports the MIB.</span></span>

<span data-ttu-id="5d7f3-107">Ogni oggetto gestito in un MIB ha un identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-107">Each managed object in a MIB has a unique identifier.</span></span> <span data-ttu-id="5d7f3-108">L'identificatore include il tipo di oggetto (ad esempio Counter, String, gauge o Address), il livello di accesso dell'oggetto, ad esempio di lettura o di lettura/scrittura, le restrizioni di dimensione e le informazioni sull'intervallo.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-108">The identifier includes the object's type (such as counter, string, gauge, or address), the object's access level (such as read or read/write), size restrictions, and range information.</span></span>

<span data-ttu-id="5d7f3-109">La tabella seguente contiene un elenco parziale dei MIB forniti con il sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-109">The following table contains a partial list of the MIBs that ship with the system.</span></span> <span data-ttu-id="5d7f3-110">Vengono installati con il servizio SNMP nella directory% SystemRoot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-110">They are installed with the SNMP service in the %systemroot%\\system32 directory.</span></span> <span data-ttu-id="5d7f3-111">Per un elenco completo di MIB, vedere il Resource Kit di Windows.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-111">For a complete listing of MIBs, refer to the Windows Resource Kit.</span></span>



| <span data-ttu-id="5d7f3-112">MIB</span><span class="sxs-lookup"><span data-stu-id="5d7f3-112">MIB</span></span>         | <span data-ttu-id="5d7f3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d7f3-113">Description</span></span>                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7f3-114">DHCP. MIB</span><span class="sxs-lookup"><span data-stu-id="5d7f3-114">DHCP.MIB</span></span>    | <span data-ttu-id="5d7f3-115">MIB definito da Microsoft che contiene i tipi di oggetto per il monitoraggio del traffico di rete tra host remoti e server DHCP</span><span class="sxs-lookup"><span data-stu-id="5d7f3-115">Microsoft-defined MIB that contains object types for monitoring the network traffic between remote hosts and DHCP servers</span></span>                        |
| <span data-ttu-id="5d7f3-116">HOSTMIB. MIB</span><span class="sxs-lookup"><span data-stu-id="5d7f3-116">HOSTMIB.MIB</span></span> | <span data-ttu-id="5d7f3-117">Contiene i tipi di oggetto per il monitoraggio e la gestione delle risorse host</span><span class="sxs-lookup"><span data-stu-id="5d7f3-117">Contains object types for monitoring and managing host resources</span></span>                                                                                 |
| <span data-ttu-id="5d7f3-118">Lmmib2. MIB</span><span class="sxs-lookup"><span data-stu-id="5d7f3-118">LMMIB2.MIB</span></span>  | <span data-ttu-id="5d7f3-119">Copre i servizi workstation e server</span><span class="sxs-lookup"><span data-stu-id="5d7f3-119">Covers workstation and server services</span></span>                                                                                                           |
| <span data-ttu-id="5d7f3-120">MIB \_ II. MIB</span><span class="sxs-lookup"><span data-stu-id="5d7f3-120">MIB\_II.MIB</span></span> | <span data-ttu-id="5d7f3-121">Contiene il Management Information Base (MIB-II), che fornisce un'architettura semplice e praticabile per la gestione di Internet basati su TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-121">Contains the Management Information Base (MIB-II), which provides a simple, workable architecture and system for managing TCP/IP-based internets</span></span> |
| <span data-ttu-id="5d7f3-122">WINS. MIB</span><span class="sxs-lookup"><span data-stu-id="5d7f3-122">WINS.MIB</span></span>    | <span data-ttu-id="5d7f3-123">MIB definito da Microsoft per Windows Internet Name Service (WINS)</span><span class="sxs-lookup"><span data-stu-id="5d7f3-123">Microsoft-defined MIB for the Windows Internet Name Service (WINS)</span></span>                                                                               |



 

<span data-ttu-id="5d7f3-124">**Windows NT:** In genere, è possibile copiare un MIB dall'agente di estensione SNMP che supporta il MIB specifico.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-124">**Windows NT:** Typically, you can copy a MIB from the SNMP extension agent that supports the particular MIB.</span></span> <span data-ttu-id="5d7f3-125">Con il Resource Kit di Windows NT 4,0 sono disponibili MIB aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-125">Some additional MIBs are available with the Windows NT 4.0 Resource Kit.</span></span>

<span data-ttu-id="5d7f3-126">Le DLL dell'agente di estensione per MIB-II, LAN Manager MIB-II e le risorse host MIB vengono installate con il servizio SNMP.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-126">The extension agent DLLs for MIB-II, LAN Manager MIB-II, and the Host Resources MIB are installed with the SNMP service.</span></span> <span data-ttu-id="5d7f3-127">Le DLL dell'agente di estensione per gli altri MIB vengono installate quando vengono installati i rispettivi servizi.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-127">The extension agent DLLs for the other MIBs are installed when their respective services are installed.</span></span> <span data-ttu-id="5d7f3-128">Al momento dell'avvio del servizio, il servizio SNMP carica tutte le DLL dell'agente di estensione elencate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-128">At service startup time, the SNMP service loads all of the extension agent DLLs that are listed in the registry.</span></span>

<span data-ttu-id="5d7f3-129">Gli utenti possono aggiungere altre DLL dell'agente di estensione che implementano MIB aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-129">Users can add other extension agent DLLs that implement additional MIBs.</span></span> <span data-ttu-id="5d7f3-130">A tale scopo, è necessario aggiungere una voce del registro di sistema per la nuova DLL nel servizio SNMP.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-130">To do this, they must add a registry entry for the new DLL under the SNMP service.</span></span> <span data-ttu-id="5d7f3-131">Devono inoltre registrare il nuovo MIB con l'applicazione console di gestione SNMP.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-131">They must also register the new MIB with the SNMP management console application.</span></span> <span data-ttu-id="5d7f3-132">Per ulteriori informazioni, vedere la documentazione inclusa nell'applicazione console di gestione.</span><span class="sxs-lookup"><span data-stu-id="5d7f3-132">For more information, see the documentation included with your management console application.</span></span>

<span data-ttu-id="5d7f3-133">Per ulteriori informazioni, vedere la pagina relativa all' [albero dei nomi MIB](mib-name-tree.md).</span><span class="sxs-lookup"><span data-stu-id="5d7f3-133">For more information, see [MIB Name Tree](mib-name-tree.md).</span></span>

 

 




