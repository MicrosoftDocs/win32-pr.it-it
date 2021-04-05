---
description: I monitoraggi ricevono i frame di rete acquisiti in modalità in tempo reale. I frame vengono acquisiti da un provider di pacchetti di rete (NPP) utilizzando l'interfaccia COM Providers IRTC e passati al monitoraggio in uno dei monitoraggi due thread di esecuzione.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Acquisizioni di Real-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885677"
---
# <a name="real-time-captures"></a><span data-ttu-id="a6d7f-104">Acquisizioni di Real-Time</span><span class="sxs-lookup"><span data-stu-id="a6d7f-104">Real-Time Captures</span></span>

<span data-ttu-id="a6d7f-105">I monitoraggi ricevono i frame di rete acquisiti in modalità in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="a6d7f-105">Monitors receive captured network frames in real-time mode.</span></span> <span data-ttu-id="a6d7f-106">I frame vengono acquisiti da un [*provider di pacchetti di rete*](n.md) (NPP) utilizzando l'interfaccia com [IRTC](irtc.md) del provider e passati al monitoraggio in uno dei due thread di esecuzione del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a6d7f-106">The frames are captured by a [*network packet provider*](n.md) (NPP) using the provider's [IRTC](irtc.md) COM interface, and passed on to the monitor in one of the monitor's two execution threads.</span></span>

<span data-ttu-id="a6d7f-107">I monitoraggi possono limitare il numero di frame da elaborare passando un filtro di [*acquisizione*](c.md) all'oggetto NPP che fornisce i frame.</span><span class="sxs-lookup"><span data-stu-id="a6d7f-107">Monitors can limit the number of frames they have to process by passing a [*capture filter*](c.md) to the NPP that is supplying the frames.</span></span> <span data-ttu-id="a6d7f-108">In genere, un monitoraggio specifico è progettato per controllare i tipi di traffico specifici, ad esempio HTTP, RIPX o SMB.</span><span class="sxs-lookup"><span data-stu-id="a6d7f-108">Typically, a specific monitor is designed to watch for specific types of traffic, such as HTTP, RIPX, or SMB.</span></span> <span data-ttu-id="a6d7f-109">Diversamente dagli esperti, che usano parser sofisticati per selezionare le informazioni da analizzare, un monitoraggio deve esaminare ogni frame per le condizioni che è stato progettato per rilevare.</span><span class="sxs-lookup"><span data-stu-id="a6d7f-109">Unlike experts, which use sophisticated parsers to select the information to be analyzed, a monitor must examine each frame for the conditions it was designed to detect.</span></span> <span data-ttu-id="a6d7f-110">Il motivo alla base di questo approccio frame per fotogramma è la prestazione.</span><span class="sxs-lookup"><span data-stu-id="a6d7f-110">The reason behind this frame-by-frame approach is performance.</span></span> <span data-ttu-id="a6d7f-111">Un monitoraggio deve elaborare i frame in modo sufficientemente rapido, in modo che non si trovino dietro il driver che fornisce i frame all'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="a6d7f-111">A monitor must process its frames quickly enough so that it does not fall behind the driver supplying the frames to the NPP.</span></span> <span data-ttu-id="a6d7f-112">In caso contrario, i dati andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="a6d7f-112">Otherwise, data will be lost.</span></span>

 

 



