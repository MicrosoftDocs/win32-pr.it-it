---
description: Panoramica dell'architettura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Panoramica dell'architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884914"
---
# <a name="architecture-overview"></a><span data-ttu-id="4156c-103">Panoramica dell'architettura</span><span class="sxs-lookup"><span data-stu-id="4156c-103">Architecture Overview</span></span>

<span data-ttu-id="4156c-104">L'architettura WPD può essere divisa in tre processi.</span><span class="sxs-lookup"><span data-stu-id="4156c-104">The WPD architecture can be divided into three processes.</span></span> <span data-ttu-id="4156c-105">All'interno di questi processi si trovano i tre componenti principali di WPD: l'API, il serializzatore e il driver.</span><span class="sxs-lookup"><span data-stu-id="4156c-105">Within these processes are the three primary components of WPD: the API, the serializer, and the driver.</span></span> <span data-ttu-id="4156c-106">Nella figura seguente vengono illustrati i processi e i componenti che costituiscono l'architettura WPD.</span><span class="sxs-lookup"><span data-stu-id="4156c-106">The following illustration depicts the processes and components that constitute the WPD architecture.</span></span>

![illustrazione che mostra i componenti API, serializer e driver di WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a><span data-ttu-id="4156c-108">Interfaccia di programmazione dell'applicazione WPD</span><span class="sxs-lookup"><span data-stu-id="4156c-108">The WPD Application Programming Interface</span></span>

<span data-ttu-id="4156c-109">L'API WPD viene implementata come un server COM in-process.</span><span class="sxs-lookup"><span data-stu-id="4156c-109">The WPD API is implemented as an in-proc COM server.</span></span> <span data-ttu-id="4156c-110">L'API usa le API Microsoft Win32 standard per comunicare con il driver WPD appropriato.</span><span class="sxs-lookup"><span data-stu-id="4156c-110">The API uses standard Microsoft Win32 APIs to communicate with the appropriate WPD driver.</span></span> <span data-ttu-id="4156c-111">Un componente denominato serializzatore WPD viene usato sia dagli oggetti API che dal driver per comprimere o decomprimere i parametri da e verso i buffer di Windows Driver Foundation (CDR)-modalità utente (UMDF).</span><span class="sxs-lookup"><span data-stu-id="4156c-111">A component called the WPD serializer is used by both API objects and the driver to pack or unpack parameters to or from Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) buffers.</span></span>

## <a name="the-wpd-serializer"></a><span data-ttu-id="4156c-112">Serializzatore WPD</span><span class="sxs-lookup"><span data-stu-id="4156c-112">The WPD Serializer</span></span>

<span data-ttu-id="4156c-113">Il serializzatore WPD viene implementato come un server COM in-process.</span><span class="sxs-lookup"><span data-stu-id="4156c-113">The WPD serializer is implemented as an in-proc COM server.</span></span> <span data-ttu-id="4156c-114">L'API WPD usa il serializzatore per comprimere i comandi e i parametri in buffer di messaggi inviati al driver.</span><span class="sxs-lookup"><span data-stu-id="4156c-114">The WPD API uses the serializer to pack commands and parameters into message buffers that are sent to the driver.</span></span> <span data-ttu-id="4156c-115">Il driver utilizza il serializzatore per decomprimere i buffer dei messaggi per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="4156c-115">The driver uses the serializer to unpack these message buffers for processing.</span></span> <span data-ttu-id="4156c-116">Il driver usa anche il serializzatore per comprimere i dati e i parametri nei buffer di risposta restituiti all'API WPD e l'API WPD usa il serializzatore per decomprimere i buffer di risposta per tornare ai chiamanti.</span><span class="sxs-lookup"><span data-stu-id="4156c-116">The driver also uses the serializer to pack data and parameters into response buffers that are returned to the WPD API, and the WPD API uses the serializer to unpack these response buffers to return to callers.</span></span>

## <a name="wpd-driver"></a><span data-ttu-id="4156c-117">Driver WPD</span><span class="sxs-lookup"><span data-stu-id="4156c-117">WPD Driver</span></span>

<span data-ttu-id="4156c-118">Il driver WPD viene implementato come driver standard di Windows Driver Foundation (CDR)-User-Mode Driver Framework (UMDF).</span><span class="sxs-lookup"><span data-stu-id="4156c-118">The WPD driver is implemented as a standard Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) driver.</span></span> <span data-ttu-id="4156c-119">I driver WPD sono ospitati da UMDF in un processo separato denominato host driver.</span><span class="sxs-lookup"><span data-stu-id="4156c-119">WPD drivers are hosted by UMDF in a separate process called the Driver Host.</span></span>

<span data-ttu-id="4156c-120">Il driver riceve i messaggi dal riflettore UMDF (questa operazione non viene mostrata nel diagramma, poiché il modo in cui vengono ricevuti i buffer non è importante per il driver.</span><span class="sxs-lookup"><span data-stu-id="4156c-120">The driver receives messages from the UMDF reflector (this is not shown in the diagram, since how the buffers are received is not important to the driver.</span></span> <span data-ttu-id="4156c-121">Per ulteriori informazioni, vedere la documentazione di UMDF.</span><span class="sxs-lookup"><span data-stu-id="4156c-121">See UMDF documentation for more information).</span></span> <span data-ttu-id="4156c-122">Il driver implementa un gestore IOCL (WPD) specifico per elaborare i messaggi WPD ricevuti dall'API WPD.</span><span class="sxs-lookup"><span data-stu-id="4156c-122">The driver implements a WPD-specific I/O Control code (IOCL) handler to process WPD messages received by the WPD API.</span></span> <span data-ttu-id="4156c-123">Il driver usa il serializzatore WPD per decomprimere i comandi e i parametri da questi buffer dei messaggi e per comprimere la risposta nel buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="4156c-123">The driver uses the WPD serializer to unpack commands and parameters from these message buffers, and to pack the response into the return buffer.</span></span>

<span data-ttu-id="4156c-124">I driver WPD possono comunicare con i dispositivi tramite un driver in modalità kernel, in genere accessibili tramite operazioni su file Win32, ovvero CreateFile, ReadFile, WriteFile e così via.</span><span class="sxs-lookup"><span data-stu-id="4156c-124">WPD drivers may communicate with their devices by going through a kernel-mode driver, typically accessed via Win32 file operations (that is, CreateFile, ReadFile, WriteFile, and so on).</span></span> <span data-ttu-id="4156c-125">Per gli autobus comuni, Microsoft fornirà i driver del kernel standard che i fornitori utilizzeranno per consentire ai fornitori di fornire una soluzione driver solo in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="4156c-125">For the common buses, Microsoft will provide standard kernel drivers for vendors to use, which will allow vendors to ship a user-mode-only driver solution.</span></span> <span data-ttu-id="4156c-126">Inoltre, per i dispositivi MTP (Media Transfer Protocol) e di classe di archiviazione di massa (MSC), Microsoft fornirà i driver della classe WPD.</span><span class="sxs-lookup"><span data-stu-id="4156c-126">In addition, for Media Transfer Protocol (MTP) and Mass Storage Class (MSC) devices, Microsoft will provide WPD class drivers.</span></span>

<span data-ttu-id="4156c-127">Per ulteriori informazioni sui driver WPD, vedere la documentazione del driver dei dispositivi portatili Windows in Windows Driver Kit.</span><span class="sxs-lookup"><span data-stu-id="4156c-127">For more information about WPD drivers, see the Windows Portable Devices Driver documentation in the Windows Driver Kit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4156c-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4156c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4156c-129">**Panoramica dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="4156c-129">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



