---
description: I controlli Call Center estendono il modello a oggetti TAPI 3 per supportare i requisiti dei sistemi di distribuzione automatica delle chiamate (ACD).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Uso di controlli Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308871"
---
# <a name="using-call-center-controls"></a><span data-ttu-id="534b2-103">Uso di controlli Call Center</span><span class="sxs-lookup"><span data-stu-id="534b2-103">Using Call Center Controls</span></span>

<span data-ttu-id="534b2-104">I controlli Call Center estendono il modello a oggetti TAPI 3 per supportare i requisiti dei sistemi di distribuzione automatica delle chiamate (ACD).</span><span class="sxs-lookup"><span data-stu-id="534b2-104">Call center controls extend the TAPI 3 object model to support the requirements of Automatic Call Distribution (ACD) systems.</span></span> <span data-ttu-id="534b2-105">Un Call Center è una località con agenti o operatori presso le banche dei telefoni, che effettuano chiamate telefoniche in uscita o che invadono in campo.</span><span class="sxs-lookup"><span data-stu-id="534b2-105">A call center is a location with agents or operators at banks of telephones either making outgoing telephone calls or fielding incoming ones.</span></span> <span data-ttu-id="534b2-106">Ad esempio, una società banca o una carta di credito utilizzerà un Call Center per elaborare le richieste di account.</span><span class="sxs-lookup"><span data-stu-id="534b2-106">For example, a bank or credit card company will use a call center to process account inquiries.</span></span>

<span data-ttu-id="534b2-107">Le applicazioni del Call Center sono divise in tre tipi di base:</span><span class="sxs-lookup"><span data-stu-id="534b2-107">Call center applications are divided into three basic types:</span></span>

-   <span data-ttu-id="534b2-108">[Proxy ACD](acd-proxy.md): gestisce le sessioni in ingresso o in uscita nel server, che può essere qualsiasi elemento da un telefono proprietario a un gateway Internet.</span><span class="sxs-lookup"><span data-stu-id="534b2-108">[ACD Proxy](acd-proxy.md): Handles incoming or outgoing sessions at the server, which can be anything from a proprietary telephone switch to an Internet gateway.</span></span>
-   <span data-ttu-id="534b2-109">[Client agente ACD](acd-agent-client.md): Servizi di un singolo agente che riceve o chiama.</span><span class="sxs-lookup"><span data-stu-id="534b2-109">[ACD Agent Client](acd-agent-client.md): Services an individual agent who is receiving or making calls.</span></span>
-   <span data-ttu-id="534b2-110">Client Supervisor ACD: fornisce una panoramica generale delle operazioni di Agent e ACD.</span><span class="sxs-lookup"><span data-stu-id="534b2-110">ACD Supervisor Client: Provides an overall view of agent and ACD operations.</span></span>

> [!Note]  
> <span data-ttu-id="534b2-111">Per Windows 2000, la funzionalità proxy è disponibile tramite TAPI 2,2 e le funzioni di Supervisore non sono implementate.</span><span class="sxs-lookup"><span data-stu-id="534b2-111">For Windows 2000, proxy functionality is available using TAPI 2.2, and supervisor functions are not implemented.</span></span>

 

<span data-ttu-id="534b2-112">La sezione Samples del Windows SDK contiene esempi di codice ACD in Netds \\ TAPI \\ Tapi2 \\ ACD e Netds \\ TAPI \\ Tapi3 \\ ACD.</span><span class="sxs-lookup"><span data-stu-id="534b2-112">The samples section of the Windows SDK contains ACD code samples under Netds\\Tapi\\Tapi2\\Acd and Netds\\Tapi\\Tapi3\\Acd.</span></span>

 

 



