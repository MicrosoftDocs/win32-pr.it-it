---
title: Dettagli dell'implementazione di DVC
description: Questa sezione contiene informazioni su come scrivere un modulo client Dynamic Channel (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298051"
---
# <a name="dvc-implementation-details"></a><span data-ttu-id="0fc59-103">Dettagli dell'implementazione di DVC</span><span class="sxs-lookup"><span data-stu-id="0fc59-103">DVC Implementation Details</span></span>

<span data-ttu-id="0fc59-104">Questa sezione contiene informazioni su come scrivere un modulo client Dynamic Channel (DVC).</span><span class="sxs-lookup"><span data-stu-id="0fc59-104">This section contains information about how to write a dynamic virtual channel (DVC) client module.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0fc59-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="0fc59-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="0fc59-106">Scrittura di un modulo client DVC</span><span class="sxs-lookup"><span data-stu-id="0fc59-106">Writing a Client DVC Module</span></span>](writing-a-client-dvc-component.md)
</dt> <dd>

<span data-ttu-id="0fc59-107">Per scrivere un modulo client Dynamic Channel (DVC), è necessario innanzitutto implementare e registrare un plug-in client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="0fc59-107">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="0fc59-108">Registrazione del plug-in DVC</span><span class="sxs-lookup"><span data-stu-id="0fc59-108">DVC plug-in registration</span></span>](dvc-plug-in-registration.md)
</dt> <dd>

<span data-ttu-id="0fc59-109">Viene descritta la sintassi per la voce del plug-in Dynamic Virtual Channel (DVC) per il client Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="0fc59-109">Describes syntax for the dynamic virtual channel (DVC) plug-in entry for the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="0fc59-110">Avvio di un listener DVC</span><span class="sxs-lookup"><span data-stu-id="0fc59-110">Starting a DVC Listener</span></span>](starting-a-dvc-listener.md)
</dt> <dd>

<span data-ttu-id="0fc59-111">Per stabilire una connessione corretta tra due moduli DVC (Dynamic Virtual Channel) in esecuzione nel client e nel server Connessione Desktop remoto (RDC), è necessario che un listener DVC sia in esecuzione e in stato di ascolto.</span><span class="sxs-lookup"><span data-stu-id="0fc59-111">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

</dd> <dt>

[<span data-ttu-id="0fc59-112">Accettazione di una connessione</span><span class="sxs-lookup"><span data-stu-id="0fc59-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> <dd>

<span data-ttu-id="0fc59-113">A un certo punto nel tempo, il client dinamico del canale virtuale (DVC) richiederà una connessione al listener di DVC.</span><span class="sxs-lookup"><span data-stu-id="0fc59-113">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span>

</dd> <dt>

[<span data-ttu-id="0fc59-114">Scrittura di dati tramite un canale DVC</span><span class="sxs-lookup"><span data-stu-id="0fc59-114">Writing Data by Using a DVC Channel</span></span>](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

<span data-ttu-id="0fc59-115">La scrittura di dati del canale tramite un canale virtuale dinamico (DVC) è simmetrica sia per il server host sessione Desktop remoto (host sessione Desktop remoto) che per il client.</span><span class="sxs-lookup"><span data-stu-id="0fc59-115">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span>

</dd> <dt>

[<span data-ttu-id="0fc59-116">Test e debug</span><span class="sxs-lookup"><span data-stu-id="0fc59-116">Testing and Debugging</span></span>](testing-and-debugging.md)
</dt> <dd>

<span data-ttu-id="0fc59-117">È presente un listener "echo" implementato dal client Connessione Desktop remoto (RDC), che è sempre presente e in ascolto delle connessioni in ingresso.</span><span class="sxs-lookup"><span data-stu-id="0fc59-117">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span>

</dd> <dt>

[<span data-ttu-id="0fc59-118">Esempio di plug-in client DVC</span><span class="sxs-lookup"><span data-stu-id="0fc59-118">DVC Client Plug-in Example</span></span>](dvc-client-plug-in-example.md)
</dt> <dd>

<span data-ttu-id="0fc59-119">Esempio di codice C++ in cui viene illustrato come creare un plug-in del canale virtuale dinamico (DVC) client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="0fc59-119">C++ code sample that shows how to create a Remote Desktop Connection (RDC) client dynamic virtual channel (DVC) plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="0fc59-120">Esempio di modulo server DVC</span><span class="sxs-lookup"><span data-stu-id="0fc59-120">DVC Server Module Example</span></span>](dvc-server-component-example.md)
</dt> <dd>

<span data-ttu-id="0fc59-121">Esempio di codice C++ che Mostra come creare il modulo canale virtuale dinamico lato server (DVC).</span><span class="sxs-lookup"><span data-stu-id="0fc59-121">C++ code sample that shows how to create the server-side dynamic virtual channel (DVC) module.</span></span>

</dd> </dl>

 

 




