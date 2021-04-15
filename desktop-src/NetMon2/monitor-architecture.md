---
description: Nella figura seguente viene illustrata la relazione tra monitoraggi e altri componenti dell'architettura Network Monitor.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Architettura di monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570681"
---
# <a name="monitor-architecture"></a><span data-ttu-id="29613-103">Architettura di monitoraggio</span><span class="sxs-lookup"><span data-stu-id="29613-103">Monitor Architecture</span></span>

<span data-ttu-id="29613-104">Nella figura seguente viene illustrata la relazione tra [*monitoraggi*](m.md) e altri componenti dell'architettura Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="29613-104">The following figure shows the relationship between [*monitors*](m.md) and other components of the Network Monitor architecture.</span></span>

![relazione tra monitoraggi e altri componenti di Network Monitor](images/nmarch2.png)

<span data-ttu-id="29613-106">Il traffico di rete viene raccolto (come singoli frame) dal driver NDIS.</span><span class="sxs-lookup"><span data-stu-id="29613-106">The network traffic is collected (as individual frames) from the NDIS driver.</span></span> <span data-ttu-id="29613-107">Il driver Network Monitor (Nmnt.sys) quindi instrada i frame a un provider di pacchetti di rete (NPP), che a sua volta acquisisce i dati in modalità in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="29613-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which in turn captures the data in real-time mode.</span></span> <span data-ttu-id="29613-108">NPP è una raccolta di interfacce COM utilizzate per acquisire i dati.</span><span class="sxs-lookup"><span data-stu-id="29613-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="29613-109">In questo caso, l'interfaccia [**IRTC**](irtc.md) viene utilizzata per eseguire un'acquisizione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="29613-109">In this case, the [**IRTC**](irtc.md) interface is used to perform a real-time capture.</span></span>

> [!Note]  
> <span data-ttu-id="29613-110">L'oggetto NPP viene usato per le acquisizioni ritardate e in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="29613-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="29613-111">Per le acquisizioni ritardate utilizzate da esperti e parser, viene utilizzata l'interfaccia [**IDelaydC**](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="29613-111">For delayed captures used by experts and parsers, the [**IDelaydC**](idelaydc.md) interface is used.</span></span>

 

<span data-ttu-id="29613-112">Il monitoraggio esamina quindi i dati acquisiti in modalità in tempo reale, individuando condizioni di rete specifiche e generando eventi in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="29613-112">The monitor then examines the captured data in real-time mode, detecting specific network conditions and generating events as required.</span></span>

<span data-ttu-id="29613-113">Gli altri tre componenti vengono utilizzati dalle applicazioni di monitoraggio, ovvero lo strumento di controllo di monitoraggio, il servizio di controllo di monitoraggio (MCSVC) e l'Visualizzatore eventi:</span><span class="sxs-lookup"><span data-stu-id="29613-113">Three other components are used by monitor applications: the Monitor Control Tool, the Monitor Control Service (MCSVC), and the Event Viewer:</span></span>

-   <span data-ttu-id="29613-114">Lo strumento di controllo di monitoraggio viene utilizzato per gestire le applicazioni di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="29613-114">The Monitor Control Tool is used to manage your monitor applications.</span></span> <span data-ttu-id="29613-115">Sono incluse la configurazione e l'esecuzione di tutte le applicazioni di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="29613-115">This includes configuring and running all your monitor applications.</span></span>
-   <span data-ttu-id="29613-116">Il servizio di controllo di monitoraggio (MCSVC) genera eventi, fornisce un collegamento di comunicazione a WMI per la visualizzazione degli eventi e coordina l'elaborazione delle operazioni di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="29613-116">The Monitor Control Service (MCSVC) fires events, provides a communications link to WMI for event viewing, and coordinates the processing of monitor operations.</span></span>
-   <span data-ttu-id="29613-117">Il Visualizzatore eventi Visualizza gli eventi generati dal servizio di controllo di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="29613-117">The Event Viewer displays the events fired by the Monitor Control Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29613-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29613-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29613-119">**IMonitor**</span><span class="sxs-lookup"><span data-stu-id="29613-119">**IMonitor**</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="29613-120">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="29613-120">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="29613-121">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="29613-121">**IRTC**</span></span>](irtc.md)
</dt> </dl>

 

 



