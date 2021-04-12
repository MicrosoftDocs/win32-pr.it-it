---
description: Network Monitor usa tre tipi di oggetti binari di grandi dimensioni (BLOB) per selezionare e connettere schede di interfaccia di rete (NIC), acquisire dati e modificare i dati di NPP.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Tipi di BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233838"
---
# <a name="blob-types"></a><span data-ttu-id="5d30c-103">Tipi di BLOB</span><span class="sxs-lookup"><span data-stu-id="5d30c-103">BLOB Types</span></span>

<span data-ttu-id="5d30c-104">Network Monitor usa tre tipi di oggetti binari di grandi dimensioni (BLOB) per selezionare e connettere schede di interfaccia di rete (NIC), acquisire dati e modificare i dati di NPP.</span><span class="sxs-lookup"><span data-stu-id="5d30c-104">Network Monitor uses three types of binary large objects (BLOBs) to select and connect network interface cards (NICs), capture data, and manipulate NPP data.</span></span>

## <a name="npp-blob"></a><span data-ttu-id="5d30c-105">BLOB NPP</span><span class="sxs-lookup"><span data-stu-id="5d30c-105">NPP BLOB</span></span>

<span data-ttu-id="5d30c-106">Le applicazioni usano i BLOB NPP per connettersi a una scheda di interfaccia di rete specifica tramite un oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="5d30c-106">Applications use NPP BLOBs to connect to a specific NIC through an NPP.</span></span> <span data-ttu-id="5d30c-107">(L'applicazione effettua la connessione con una chiamata a **CreateNPPInterface** e ai dati relativi alla posizione nel BLOB di NPP). Un'applicazione può inoltre archiviare i dati di configurazione nel BLOB NPP per configurare l'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="5d30c-107">(The application makes the connection with a call to **CreateNPPInterface** and location data in the NPP BLOB.) An application can also store its configuration data in the NPP BLOB to configure the NPP.</span></span> <span data-ttu-id="5d30c-108">Inoltre, un'applicazione che salva il BLOB di NPP non deve passare attraverso il Finder per riutilizzare tale BLOB.</span><span class="sxs-lookup"><span data-stu-id="5d30c-108">Also, an application that saves its NPP BLOB is not required to go through the Finder to reuse that BLOB.</span></span>

## <a name="filter-blob"></a><span data-ttu-id="5d30c-109">Filtra BLOB</span><span class="sxs-lookup"><span data-stu-id="5d30c-109">Filter BLOB</span></span>

<span data-ttu-id="5d30c-110">Un BLOB di filtri contiene criteri definiti dall'applicazione che è possibile usare per selezionare un oggetto NPP e una scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="5d30c-110">A filter BLOB contains application-defined criteria that you can use to select an NPP and a NIC.</span></span> <span data-ttu-id="5d30c-111">Ad esempio, un'applicazione può richiedere una scheda di interfaccia di rete specifica, solo schede Ethernet o schede che supportano una frequenza di acquisizione dei frame specifica.</span><span class="sxs-lookup"><span data-stu-id="5d30c-111">For example, an application can request a specific NIC, only Ethernet cards, or cards that support a specific frame capture rate.</span></span>

## <a name="special-blob"></a><span data-ttu-id="5d30c-112">BLOB speciale</span><span class="sxs-lookup"><span data-stu-id="5d30c-112">Special BLOB</span></span>

<span data-ttu-id="5d30c-113">Quando un NPP richiede dati aggiuntivi prima di poter restituire un BLOB NPP a un'applicazione, l'oggetto NPP usa un BLOB speciale.</span><span class="sxs-lookup"><span data-stu-id="5d30c-113">When an NPP requires additional data before it can return an NPP BLOB to an application, the NPP uses a special BLOB.</span></span> <span data-ttu-id="5d30c-114">In genere, l'applicazione non necessita né USA BLOB speciali, quindi non viene restituita a un'applicazione a meno che non sia impostato un flag specifico in una chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="5d30c-114">Most often, the application will not need or use special BLOBs so they are not returned to an application unless a specific flag is set in one function call.</span></span> <span data-ttu-id="5d30c-115">Ad esempio, un NPP remoto usa un BLOB speciale perché è necessario un nome di percorso per effettuare una connessione.</span><span class="sxs-lookup"><span data-stu-id="5d30c-115">For example, a remote NPP uses a special BLOB because a path name is required to make a connection.</span></span> <span data-ttu-id="5d30c-116">Un'applicazione che riceve un BLOB speciale NPP remoto può aggiungere la stringa e richiamarla nel Finder per ottenere una tabella BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="5d30c-116">An application that receives a remote NPP special BLOB could add the string and call back into the Finder to get an NPP BLOB table.</span></span> <span data-ttu-id="5d30c-117">Per altre informazioni, vedere [voci speciali](special-blob-entries.md)per i BLOB.</span><span class="sxs-lookup"><span data-stu-id="5d30c-117">For more information, see [Special BLOB Entries](special-blob-entries.md).</span></span>

 

 



