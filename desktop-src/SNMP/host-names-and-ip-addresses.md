---
title: Nomi host e indirizzi IP
description: Le reti TCP/IP richiedono la risoluzione dei nomi host negli indirizzi IP prima che sia possibile utilizzare le informazioni sull'indirizzo per creare una connessione.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Indirizzi IP e nomi host SNMP
- Nomi host, risoluzione SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709580"
---
# <a name="host-names-and-ip-addresses"></a><span data-ttu-id="b946e-105">Nomi host e indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="b946e-105">Host Names and IP Addresses</span></span>

<span data-ttu-id="b946e-106">Le reti TCP/IP richiedono la risoluzione dei nomi host negli indirizzi IP prima che sia possibile utilizzare le informazioni sull'indirizzo per creare una connessione.</span><span class="sxs-lookup"><span data-stu-id="b946e-106">TCP/IP networks require host names to be resolved to IP addresses before the address information can be used to create a connection.</span></span> <span data-ttu-id="b946e-107">Nei computer che eseguono il sistema operativo Windows viene utilizzato un file host che, a tale scopo, esegue il mapping dei nomi host agli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="b946e-107">Computers running on the Windows operating system use a host file that, for this purpose, maps host names to IP addresses.</span></span>

<span data-ttu-id="b946e-108">Il file host è un file di testo in cui sono elencati i nomi host e gli indirizzi IP espliciti.</span><span class="sxs-lookup"><span data-stu-id="b946e-108">The host file is a text file that lists explicit host names and IP addresses.</span></span> <span data-ttu-id="b946e-109">Il file host viene caricato automaticamente in memoria all'avvio e viene consultato quando è necessario risolvere un nome host.</span><span class="sxs-lookup"><span data-stu-id="b946e-109">The host file is automatically loaded into memory on startup and consulted when a host name requires resolution.</span></span> <span data-ttu-id="b946e-110">Se il file host non contiene le informazioni di mapping necessarie per risolvere un nome host specifico nel relativo indirizzo IP, viene eseguita una query di risoluzione su un server DNS.</span><span class="sxs-lookup"><span data-stu-id="b946e-110">If the host file does not contain the mapping information that is required to resolve a specific host name to its IP address, a resolution query is made to a DNS server.</span></span>

<span data-ttu-id="b946e-111">SNMP usa Windows Internet Naming Service (WINS) per la risoluzione dei nomi host.</span><span class="sxs-lookup"><span data-stu-id="b946e-111">SNMP uses the Windows Internet Naming Service (WINS) for host name resolution.</span></span> <span data-ttu-id="b946e-112">WINS consente di eseguire il mapping di nomi NetBIOS o nomi di computer a indirizzi IP su reti TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b946e-112">WINS makes it possible to map NetBIOS names, or machine names, to IP addresses on TCP/IP networks.</span></span> <span data-ttu-id="b946e-113">Se il computer non è in grado di accedere a un server WINS, il servizio SNMP utilizza il file host per risolvere i nomi host in indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="b946e-113">If the computer cannot access a WINS server, the SNMP service uses the host file to resolve host names to IP addresses.</span></span>

<span data-ttu-id="b946e-114">Il servizio SNMP supporta l'utilizzo di nomi host e indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="b946e-114">The SNMP service supports the use of both host names and IP addresses.</span></span> <span data-ttu-id="b946e-115">Tuttavia, quando è possibile scegliere tra l'utilizzo di nomi host o indirizzi IP per identificare i percorsi di rete, le applicazioni di gestione SNMP devono utilizzare nomi host.</span><span class="sxs-lookup"><span data-stu-id="b946e-115">However, when you have a choice between using host names or IP addresses to identify network locations, your SNMP management applications should use host names.</span></span> <span data-ttu-id="b946e-116">Se si utilizzano nomi host, aggiungere tutti i mapping di nome host e indirizzo IP dei sistemi partecipanti al file host.</span><span class="sxs-lookup"><span data-stu-id="b946e-116">If you use host names, add all host name and IP address mappings of the participating systems to the host file.</span></span>

 

 




