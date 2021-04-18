---
description: Microsoft Telephony Application Programming Interface (TAPI) versione 3,1 è un'API basata su Component Object Model (COM) che unisce la telefonia classica e IP.
ms.assetid: 79c4d2c9-953e-4e68-98b7-6a0dd9a04e0b
title: Telephony Application Programming Interface versione 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d302f6ffe67094d436caf94cc8cf109e1e3c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315795"
---
# <a name="telephony-application-programming-interface-version-31"></a><span data-ttu-id="46465-103">Telephony Application Programming Interface versione 3,1</span><span class="sxs-lookup"><span data-stu-id="46465-103">Telephony Application Programming Interface Version 3.1</span></span>

## <a name="purpose"></a><span data-ttu-id="46465-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="46465-104">Purpose</span></span>

<span data-ttu-id="46465-105">Microsoft Telephony Application Programming Interface (TAPI) versione 3,1 è un'API basata su Component Object Model (COM) che unisce la telefonia classica e IP.</span><span class="sxs-lookup"><span data-stu-id="46465-105">The Microsoft Telephony Application Programming Interface (TAPI) version 3.1 is a Component Object Model (COM)-based API that merges classic and IP telephony.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="46465-106">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="46465-106">Where applicable</span></span>

<span data-ttu-id="46465-107">Le applicazioni TAPI possibili includono:</span><span class="sxs-lookup"><span data-stu-id="46465-107">Possible TAPI applications include:</span></span>

-   <span data-ttu-id="46465-108">Comunicazione IP multimediale multicast con qualità del servizio (QOS)</span><span class="sxs-lookup"><span data-stu-id="46465-108">Multicast multimedia IP conferencing with quality of service (QOS)</span></span>
-   <span data-ttu-id="46465-109">Chiamate vocali su Internet tramite il protocollo H. 323</span><span class="sxs-lookup"><span data-stu-id="46465-109">Voice calls over the Internet using the H.323 protocol</span></span>
-   <span data-ttu-id="46465-110">Applicazioni Call Center in grado di tenere traccia di più agenti</span><span class="sxs-lookup"><span data-stu-id="46465-110">Call center applications capable of tracking multiple agents</span></span>
-   <span data-ttu-id="46465-111">Chiamate vocali di base sulla rete telefonica a commutazione pubblica (PSTN)</span><span class="sxs-lookup"><span data-stu-id="46465-111">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="46465-112">Controllo PBX</span><span class="sxs-lookup"><span data-stu-id="46465-112">PBX control</span></span>
-   <span data-ttu-id="46465-113">Sistemi IVR (Interactive Voice Response)</span><span class="sxs-lookup"><span data-stu-id="46465-113">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="46465-114">Messaggi vocali</span><span class="sxs-lookup"><span data-stu-id="46465-114">Voice mail</span></span>

## <a name="developer-audience"></a><span data-ttu-id="46465-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="46465-115">Developer audience</span></span>

<span data-ttu-id="46465-116">È possibile scrivere applicazioni abilitate per TAPI in molti linguaggi, tra cui Java, Visual Basic e C/C++.</span><span class="sxs-lookup"><span data-stu-id="46465-116">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="46465-117">È necessaria una certa familiarità con COM.</span><span class="sxs-lookup"><span data-stu-id="46465-117">Familiarity with COM is required.</span></span> <span data-ttu-id="46465-118">L'esperienza di sviluppo con le telecomunicazioni o altre applicazioni di telefonia è utile, ma non necessaria.</span><span class="sxs-lookup"><span data-stu-id="46465-118">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="46465-119">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="46465-119">Run-time requirements</span></span>

<span data-ttu-id="46465-120">La versione 3,1 di TAPI consente lo sviluppo di applicazioni di comunicazione per i sistemi operativi Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="46465-120">TAPI version 3.1 enables development of communications applications for Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="46465-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="46465-121">In this section</span></span>



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="46465-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="46465-122">Topic</span></span></th><th><span data-ttu-id="46465-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46465-123">Description</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="46465-124"><a href="tapi-3-1-overview.md">Overview</a></span><span class="sxs-lookup"><span data-stu-id="46465-124"><a href="tapi-3-1-overview.md">Overview</a></span></span><br/></td><td><span data-ttu-id="46465-125">Informazioni generali sull'architettura e i componenti TAPI.</span><span class="sxs-lookup"><span data-stu-id="46465-125">General information about TAPI architecture and components.</span></span><br/></td></tr><tr class="even"><td><span data-ttu-id="46465-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="46465-126">Reference</span></span><br/></td><td><span data-ttu-id="46465-127">Documentazione per:</span><span class="sxs-lookup"><span data-stu-id="46465-127">Documentation for:</span></span><br/><ul><li><span data-ttu-id="46465-128"><a href="call-and-media-controls-reference.md">Riferimento ai controlli Call e media</a></span><span class="sxs-lookup"><span data-stu-id="46465-128"><a href="call-and-media-controls-reference.md">Call and Media Controls Reference</a></span></span></li><li><span data-ttu-id="46465-129"><a href="call-center-controls-reference.md">Riferimento ai controlli Call Center</a></span><span class="sxs-lookup"><span data-stu-id="46465-129"><a href="call-center-controls-reference.md">Call Center Controls Reference</a></span></span></li><li><span data-ttu-id="46465-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Riferimento Rendezvous</a></span><span class="sxs-lookup"><span data-stu-id="46465-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Rendezvous Reference</a></span></span></li></ul></td></tr></tbody></table>



 

## <a name="related-topics"></a><span data-ttu-id="46465-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46465-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46465-132">Panoramica della telefonia Microsoft</span><span class="sxs-lookup"><span data-stu-id="46465-132">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="46465-133">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="46465-133">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="46465-134">Provider di servizi TAPI</span><span class="sxs-lookup"><span data-stu-id="46465-134">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

