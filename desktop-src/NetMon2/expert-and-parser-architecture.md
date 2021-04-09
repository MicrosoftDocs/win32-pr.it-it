---
description: Nella figura seguente viene illustrata la relazione tra le applicazioni Expert e parser e altri componenti dell'architettura Network Monitor.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Architettura di esperti e parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128362"
---
# <a name="expert-and-parser-architecture"></a><span data-ttu-id="dfdd9-103">Architettura di esperti e parser</span><span class="sxs-lookup"><span data-stu-id="dfdd9-103">Expert and Parser Architecture</span></span>

<span data-ttu-id="dfdd9-104">Nella figura seguente viene illustrata la relazione tra le applicazioni [Expert](experts.md) e [parser](parsers.md) e altri componenti dell'architettura Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="dfdd9-104">The following figure shows the relationship between [expert](experts.md) and [parser](parsers.md) applications and other components of the Network Monitor architecture.</span></span>

![relazione tra le applicazioni Expert e parser](images/nm-arch1.png)

<span data-ttu-id="dfdd9-106">Il traffico di rete viene raccolto come singoli frame dal driver NDIS.</span><span class="sxs-lookup"><span data-stu-id="dfdd9-106">The network traffic is collected, as individual frames, from the NDIS driver.</span></span> <span data-ttu-id="dfdd9-107">Il driver Network Monitor (Nmnt.sys) quindi instrada i frame a un provider di pacchetti di rete (NPP), che acquisisce i dati e li inserisce in uno o più file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dfdd9-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which captures the data and places it in one or more capture files.</span></span> <span data-ttu-id="dfdd9-108">NPP è una raccolta di interfacce COM utilizzate per acquisire i dati.</span><span class="sxs-lookup"><span data-stu-id="dfdd9-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="dfdd9-109">In questo caso, l'interfaccia [**IDelaydC**](idelaydc.md) viene utilizzata per eseguire un'acquisizione ritardata.</span><span class="sxs-lookup"><span data-stu-id="dfdd9-109">In this case, the [**IDelaydC**](idelaydc.md) interface is used to perform a delayed capture.</span></span>

> [!Note]  
> <span data-ttu-id="dfdd9-110">L'oggetto NPP viene usato per le acquisizioni ritardate e in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="dfdd9-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="dfdd9-111">Per le acquisizioni in tempo reale, viene usata l'interfaccia [**IRTC**](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="dfdd9-111">For real-time captures, the [**IRTC**](irtc.md) interface is used.</span></span>

 

<span data-ttu-id="dfdd9-112">Quando i frame di rete vengono archiviati nel file di acquisizione e il file è accessibile, gli esperti e i parser possono utilizzare l'interfaccia utente di Network Monitor e le funzioni Network Monitor fornite in Nmapi.dll per analizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="dfdd9-112">When the network frames are stored in the capture file and the file is accessible, experts and parsers can use the Network Monitor UI and the Network Monitor functions provided in Nmapi.dll to analyze the data.</span></span> <span data-ttu-id="dfdd9-113">I file di acquisizione non sono accessibili fino al completamento dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dfdd9-113">Capture files are not accessible until the capture is complete.</span></span>

 

 



