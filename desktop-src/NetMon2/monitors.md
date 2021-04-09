---
description: Un monitoraggio è una libreria a collegamento dinamico (DLL) che esamina le acquisizioni in tempo reale del traffico di rete.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitoraggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966768"
---
# <a name="monitors"></a><span data-ttu-id="e46e4-103">Monitoraggi</span><span class="sxs-lookup"><span data-stu-id="e46e4-103">Monitors</span></span>

<span data-ttu-id="e46e4-104">Un monitoraggio è una libreria a collegamento dinamico (DLL) che esamina le acquisizioni in tempo reale del traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="e46e4-104">A monitor is a dynamic-link library (DLL) that examines real-time captures of network traffic.</span></span> <span data-ttu-id="e46e4-105">Cerca le condizioni predefinite e quindi genera eventi quando vengono rilevate tali condizioni.</span><span class="sxs-lookup"><span data-stu-id="e46e4-105">It searches for pre-defined conditions and then generates events when those conditions are detected.</span></span> <span data-ttu-id="e46e4-106">Ad esempio, un evento può essere generato quando si tenta di eseguire un'operazione di failover di rete, quando una workstation non autorizzata distribuisce indirizzi IP o quando un router non riesce.</span><span class="sxs-lookup"><span data-stu-id="e46e4-106">For example, an event may be fired when a network break-in is attempted, when a rogue workstation is handing out IP addresses, or when a router fails.</span></span>

> [!Note]  
> <span data-ttu-id="e46e4-107">Se è necessario eseguire analisi dettagliate sui dati di rete che richiedono un'analisi di post-acquisizione, è necessario usare applicazioni di [*esperti*](e.md) e [*parser*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="e46e4-107">If you need to perform detailed analyses on network data that requires a post-capture analysis, you must use [*expert*](e.md) and [*parser*](p.md) applications.</span></span>

 

<span data-ttu-id="e46e4-108">Il [*servizio di controllo di monitoraggio*](m.md) (MCSVC) fornisce il Framework per la gestione dei monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="e46e4-108">The [*Monitor Control Service*](m.md) (MCSVC) provides the framework for managing your monitors.</span></span> <span data-ttu-id="e46e4-109">Fornisce funzioni per caricare le DLL di monitoraggio e un'interfaccia di comunicazione per lo strumento di controllo del monitoraggio, in modo da poter creare, configurare, avviare, arrestare e disabilitare più istanze dei monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="e46e4-109">It provides functions to load the monitor DLLs, and a communications interface to the Monitor Control Tool so that you can create, configure, start, stop, and disable multiple instances of your monitors.</span></span>

<span data-ttu-id="e46e4-110">I monitoraggi vengono eseguiti in due thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e46e4-110">Monitors run in two threads of execution.</span></span> <span data-ttu-id="e46e4-111">MCSVC fornisce il primo thread, che fornisce il controllo diretto del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="e46e4-111">The MCSVC provides the first thread, which provides direct control of the monitor.</span></span> <span data-ttu-id="e46e4-112">Il secondo thread viene fornito dal [*provider di pacchetti di rete*](n.md) (NPP), che fornisce un modo per passare i dati di rete acquisiti, le statistiche e lo stato dell'acquisizione dall'oggetto NPP al monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="e46e4-112">The second thread is provided by the [*network packet provider*](n.md) (NPP), which provides a way to pass the captured network data, statistics, and the status of the capture from the NPP back to the monitor.</span></span>

<span data-ttu-id="e46e4-113">Per ogni interfaccia NPP di runtime utilizzata per l'acquisizione dei dati può esistere più di un'istanza dello stesso monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="e46e4-113">More than one instance of the same monitor can exist for each run-time NPP interface used to capture data.</span></span>

 

 



