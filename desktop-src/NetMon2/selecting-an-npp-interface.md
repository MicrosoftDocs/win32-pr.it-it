---
description: I provider di pacchetti di rete (centrali) espongono le interfacce IDelaydC, IESP, IRTC e IStats.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Selezione di un'interfaccia NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880702"
---
# <a name="selecting-an-npp-interface"></a><span data-ttu-id="f67e4-103">Selezione di un'interfaccia NPP</span><span class="sxs-lookup"><span data-stu-id="f67e4-103">Selecting an NPP Interface</span></span>

<span data-ttu-id="f67e4-104">I provider di pacchetti di rete (centrali) espongono le interfacce [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md)e [**IStats**](istats.md) .</span><span class="sxs-lookup"><span data-stu-id="f67e4-104">Network packet providers (NPPs) expose the [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md), and [**IStats**](istats.md) interfaces.</span></span> <span data-ttu-id="f67e4-105">Ognuna di queste interfacce fornisce metodi simili per connettere l'oggetto NPP alla rete, acquisire il traffico di rete e raccogliere informazioni statistiche sui dati acquisiti.</span><span class="sxs-lookup"><span data-stu-id="f67e4-105">Each of these interfaces provides similar methods for connecting the NPP to the network, capturing network traffic, and collecting statistical information about the captured data.</span></span> <span data-ttu-id="f67e4-106">Per scegliere l'interfaccia da utilizzare, fare riferimento alla tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f67e4-106">To choose which interface to use, refer to the following table.</span></span>

> [!Note]  
> <span data-ttu-id="f67e4-107">Quando si connette un oggetto NPP alla rete con una di queste interfacce, è possibile utilizzare solo i metodi forniti da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f67e4-107">When you connect an NPP to the network with one of these interfaces, you can only use the methods provided by that interface.</span></span> <span data-ttu-id="f67e4-108">Se ad esempio ci si connette alla rete usando l'interfaccia [**IRTC**](irtc.md) e quindi si prova ad avviare un'acquisizione con [**IDelaydC**](idelaydc.md), la chiamata per avviare l'acquisizione avrà esito negativo e verrà restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="f67e4-108">For example, if you connect to the network using the [**IRTC**](irtc.md) interface and then try to start a capture with [**IDelaydC**](idelaydc.md), your call to start the capture will fail, and an error code will be returned.</span></span>

 



| <span data-ttu-id="f67e4-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f67e4-109">Interface</span></span>                    | <span data-ttu-id="f67e4-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f67e4-110">When to use</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f67e4-111">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="f67e4-111">**IDelaydC**</span></span>](idelaydc.md) | <span data-ttu-id="f67e4-112">Usare per acquisire il traffico di rete e archiviarlo in un file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f67e4-112">Use to capture network traffic and store it in a capture file.</span></span> <span data-ttu-id="f67e4-113">Questa interfaccia viene utilizzata dall'interfaccia utente di Network Monitor e da altre applicazioni NPP, che richiedono l'archiviazione delle informazioni di rete acquisite.</span><span class="sxs-lookup"><span data-stu-id="f67e4-113">This interface is used by the Network Monitor UI and other NPP applications, which require storing captured network information.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="f67e4-114">**IESP**</span><span class="sxs-lookup"><span data-stu-id="f67e4-114">**IESP**</span></span>](iesp.md)         | <span data-ttu-id="f67e4-115">Utilizzato per fornire statistiche avanzate in un formato di file ESP speciale.</span><span class="sxs-lookup"><span data-stu-id="f67e4-115">Used to provide enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="f67e4-116">Questa interfaccia viene utilizzata dalle applicazioni NPP che richiedono le statistiche avanzate fornite dal formato ESP.</span><span class="sxs-lookup"><span data-stu-id="f67e4-116">This interface is used by NPP applications that require the enhanced statistics provided by the ESP format.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="f67e4-117">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="f67e4-117">**IRTC**</span></span>](irtc.md)         | <span data-ttu-id="f67e4-118">Usare per acquisire il traffico di rete in tempo reale e per attivare eventi quando si verificano.</span><span class="sxs-lookup"><span data-stu-id="f67e4-118">Use to capture real-time network traffic and to trigger events when they occur.</span></span> <span data-ttu-id="f67e4-119">Questa interfaccia viene utilizzata dalle applicazioni NPP che richiedono acquisizioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f67e4-119">This interface is used by NPP applications that require run-time captures.</span></span> <span data-ttu-id="f67e4-120">Si noti che questa interfaccia non fornisce le statistiche fornite dalle altre interfacce di NPP, né consente di inserire frame nel traffico di rete acquisito.</span><span class="sxs-lookup"><span data-stu-id="f67e4-120">Note that this interface does not provide the statistics that the other NPP interfaces provide, nor does it allow you to insert frames into the captured network traffic.</span></span><br/> |
| [<span data-ttu-id="f67e4-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="f67e4-121">**IStats**</span></span>](istats.md)     | <span data-ttu-id="f67e4-122">Usare per recuperare le statistiche di acquisizione ma non i frame acquisiti.</span><span class="sxs-lookup"><span data-stu-id="f67e4-122">Use to retrieve capture statistics but not the captured frames.</span></span>                                                                                                                                                                                                                                                                                 |



 

 

 




