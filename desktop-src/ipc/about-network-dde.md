---
description: La rete DDE viene utilizzata per avviare e gestire le connessioni di rete necessarie per le conversazioni DDE tra le applicazioni in esecuzione in computer diversi in una rete.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Informazioni su DDE di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345086"
---
# <a name="about-network-dde"></a><span data-ttu-id="85a6e-103">Informazioni su DDE di rete</span><span class="sxs-lookup"><span data-stu-id="85a6e-103">About Network DDE</span></span>

<span data-ttu-id="85a6e-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="85a6e-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="85a6e-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="85a6e-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="85a6e-106">La rete DDE viene utilizzata per avviare e gestire le connessioni di rete necessarie per le conversazioni DDE tra le applicazioni in esecuzione in computer diversi in una rete.</span><span class="sxs-lookup"><span data-stu-id="85a6e-106">Network DDE is used to initiate and maintain the network connections needed for DDE conversations between applications running on different computers in a network.</span></span> <span data-ttu-id="85a6e-107">Una *conversazione* DDE è l'interazione tra applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="85a6e-107">A DDE *conversation* is the interaction between client and server applications.</span></span> <span data-ttu-id="85a6e-108">Utilizzare la rete DDE insieme a DDE e la libreria di gestione DDE (DDEML) nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="85a6e-108">You use network DDE along with DDE and the DDE management library (DDEML) in your application.</span></span>

<span data-ttu-id="85a6e-109">DDE è una forma di comunicazione interprocesso che utilizza la memoria condivisa per scambiare dati tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="85a6e-109">DDE is a form of interprocess communication that uses shared memory to exchange data between applications.</span></span> <span data-ttu-id="85a6e-110">Le applicazioni possono utilizzare DDE per i trasferimenti di dati una volta o per gli scambi in corso e per l'aggiornamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="85a6e-110">Applications can use DDE for one time data transfers or for ongoing exchanges and updating data.</span></span> <span data-ttu-id="85a6e-111">Per ulteriori informazioni su DDE, vedere [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="85a6e-111">For more information on DDE, see [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).</span></span>

<span data-ttu-id="85a6e-112">DDEML semplifica l'attività di aggiunta della funzionalità DDE a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="85a6e-112">DDEML simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="85a6e-113">Anziché inviare, inviare ed elaborare direttamente i messaggi DDE, un'applicazione utilizza le funzioni fornite da DDEML per gestire le conversazioni DDE.</span><span class="sxs-lookup"><span data-stu-id="85a6e-113">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="85a6e-114">Per ulteriori informazioni su DDEML, vedere [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span><span class="sxs-lookup"><span data-stu-id="85a6e-114">For more information on DDEML, see [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span></span>

## <a name="network-dde-files"></a><span data-ttu-id="85a6e-115">File DDE di rete</span><span class="sxs-lookup"><span data-stu-id="85a6e-115">Network DDE Files</span></span>

<span data-ttu-id="85a6e-116">Per usare gli elementi API del DDE di rete, è necessario includere il file di intestazione NDDEApi. h nei file di origine e includere il file NDDEApi. lib nella riga di collegamento.</span><span class="sxs-lookup"><span data-stu-id="85a6e-116">To use the API elements of network DDE, you must include the NDDEApi.h header file in your source files and include NDDEApi.lib file on your link line.</span></span> <span data-ttu-id="85a6e-117">È inoltre necessario assicurarsi che il file di NDDEApi.dll venga caricato.</span><span class="sxs-lookup"><span data-stu-id="85a6e-117">You must also make sure that the NDDEApi.dll file is loaded.</span></span>

<span data-ttu-id="85a6e-118">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="85a6e-118">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="85a6e-119">Agente DDE di rete</span><span class="sxs-lookup"><span data-stu-id="85a6e-119">Network DDE Agent</span></span>](network-dde-agent.md)
-   [<span data-ttu-id="85a6e-120">Condivisioni DDE</span><span class="sxs-lookup"><span data-stu-id="85a6e-120">DDE Shares</span></span>](dde-shares.md)
-   [<span data-ttu-id="85a6e-121">Condivisioni attendibili e sicurezza</span><span class="sxs-lookup"><span data-stu-id="85a6e-121">Trusted Shares and Security</span></span>](trusted-shares-and-security.md)
-   [<span data-ttu-id="85a6e-122">Gestione delle condivisioni DDE</span><span class="sxs-lookup"><span data-stu-id="85a6e-122">Managing DDE Shares</span></span>](managing-dde-shares.md)

 

 
