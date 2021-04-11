---
title: Ascolto degli eventi della barra multifunzione
description: Il Framework della barra multifunzione di Windows usa l'infrastruttura Event Tracing for Windows (ETW) per consentire agli sviluppatori di apprendere il modo in cui gli utenti interagiscono con la barra multifunzione dell'applicazione.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Barra multifunzione di Windows, eventi
- Barra multifunzione, eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339447"
---
# <a name="listening-for-ribbon-events"></a><span data-ttu-id="d67b1-105">Ascolto degli eventi della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="d67b1-105">Listening for Ribbon Events</span></span>

<span data-ttu-id="d67b1-106">Il Framework della barra multifunzione di Windows usa l'infrastruttura [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) per consentire agli sviluppatori di apprendere il modo in cui gli utenti interagiscono con la barra multifunzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d67b1-106">The Windows Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="introduction"></a><span data-ttu-id="d67b1-107">Introduzione</span><span class="sxs-lookup"><span data-stu-id="d67b1-107">Introduction</span></span>

<span data-ttu-id="d67b1-108">Il meccanismo degli eventi della barra multifunzione è progettato in modo che il Framework segnali gli eventi dell'interfaccia utente della barra multifunzione all'applicazione, in modo da poter monitorare le attività degli utenti, apprendere i modelli di interazione e valutare le tendenze</span><span class="sxs-lookup"><span data-stu-id="d67b1-108">The Ribbon framework event mechanism is designed such that the framework reports ribbon UI events to the application so you can monitor user activity, learn their interaction patterns, and assess usage trends.</span></span> <span data-ttu-id="d67b1-109">Queste informazioni possono essere usate per ottimizzare l'esperienza utente per le iterazioni future dell'app della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d67b1-109">This information can be used to refine the user experience for future iterations of your ribbon app.</span></span>

<span data-ttu-id="d67b1-110">L'utilizzo degli eventi del Framework della barra multifunzione prevede quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d67b1-110">Using the Ribbon framework events involves the following:</span></span>

1.  <span data-ttu-id="d67b1-111">L'applicazione Ribbon deve registrare un listener di [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) per ricevere le notifiche degli eventi della barra multifunzione dal framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d67b1-111">The ribbon application must register an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener to receive ribbon event notifications from the Ribbon framework.</span></span>
2.  <span data-ttu-id="d67b1-112">Il Framework della barra multifunzione attiva i callback degli eventi dell'interfaccia utente della barra multifunzione in fase di esecuzione, se l'applicazione ha registrato un listener di [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d67b1-112">The Ribbon framework fires ribbon UI event callbacks at run time, if the application has registered an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener.</span></span>

## <a name="supported-events"></a><span data-ttu-id="d67b1-113">Eventi supportati</span><span class="sxs-lookup"><span data-stu-id="d67b1-113">Supported events</span></span>

<span data-ttu-id="d67b1-114">Gli eventi esposti alle applicazioni della barra multifunzione sono descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d67b1-114">The events exposed to ribbon applications are described in the following table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d67b1-115">Evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-115">Event</span></span></th>
<th><span data-ttu-id="d67b1-116">Report eventi</span><span class="sxs-lookup"><span data-stu-id="d67b1-116">Event report</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d67b1-117">Scheda attivata</span><span class="sxs-lookup"><span data-stu-id="d67b1-117">Tab activated</span></span></td>
<td><span data-ttu-id="d67b1-118">ID comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-118">Command ID</span></span><br/> <span data-ttu-id="d67b1-119">Nome comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-119">Command name</span></span><br/> <span data-ttu-id="d67b1-120">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-120">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d67b1-121">Scheda contestuale attivata</span><span class="sxs-lookup"><span data-stu-id="d67b1-121">Contextual tab activated</span></span></td>
<td><span data-ttu-id="d67b1-122">ID comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-122">Command ID</span></span><br/> <span data-ttu-id="d67b1-123">Nome comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-123">Command name</span></span><br/> <span data-ttu-id="d67b1-124">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-124">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d67b1-125">Menu applicazione aperto</span><span class="sxs-lookup"><span data-stu-id="d67b1-125">Application Menu opened</span></span></td>
<td><span data-ttu-id="d67b1-126">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-126">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d67b1-127">Menu applicazione chiuso</span><span class="sxs-lookup"><span data-stu-id="d67b1-127">Application Menu closed</span></span></td>
<td><span data-ttu-id="d67b1-128">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-128">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d67b1-129">Menu (Regular o Gallery) aperto</span><span class="sxs-lookup"><span data-stu-id="d67b1-129">Menu (regular or gallery) opened</span></span></td>
<td><span data-ttu-id="d67b1-130">ID comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-130">Command ID</span></span><br/> <span data-ttu-id="d67b1-131">Nome comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-131">Command name</span></span><br/> <span data-ttu-id="d67b1-132">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-132">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d67b1-133">Gli eventi del menu QAT non sono esposti.</span><span class="sxs-lookup"><span data-stu-id="d67b1-133">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d67b1-134">Menu (Regular o Gallery) chiuso</span><span class="sxs-lookup"><span data-stu-id="d67b1-134">Menu (regular or gallery) closed</span></span></td>
<td><span data-ttu-id="d67b1-135">ID comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-135">Command ID</span></span><br/> <span data-ttu-id="d67b1-136">Nome comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-136">Command name</span></span><br/> <span data-ttu-id="d67b1-137">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-137">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d67b1-138">Gli eventi del menu QAT non sono esposti.</span><span class="sxs-lookup"><span data-stu-id="d67b1-138">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d67b1-139">Comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-139">Command</span></span></td>
<td><span data-ttu-id="d67b1-140">ID comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-140">Command ID</span></span><br/> <span data-ttu-id="d67b1-141">Nome comando</span><span class="sxs-lookup"><span data-stu-id="d67b1-141">Command name</span></span><br/> <span data-ttu-id="d67b1-142">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-142">Event verb</span></span><br/> <span data-ttu-id="d67b1-143">Uno dei percorsi degli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d67b1-143">One of the following event locations:</span></span>
<ul>
<li><span data-ttu-id="d67b1-144">RIBBON</span><span class="sxs-lookup"><span data-stu-id="d67b1-144">RIBBON</span></span></li>
<li><span data-ttu-id="d67b1-145">QUICKACCESSTOOLBAR</span><span class="sxs-lookup"><span data-stu-id="d67b1-145">QUICKACCESSTOOLBAR</span></span></li>
<li><span data-ttu-id="d67b1-146">APPLICATIONMENU</span><span class="sxs-lookup"><span data-stu-id="d67b1-146">APPLICATIONMENU</span></span></li>
<li><span data-ttu-id="d67b1-147">CONTEXTPOPUP</span><span class="sxs-lookup"><span data-stu-id="d67b1-147">CONTEXTPOPUP</span></span></li>
</ul>
<br/> <span data-ttu-id="d67b1-148">ID comando padre</span><span class="sxs-lookup"><span data-stu-id="d67b1-148">Parent Command ID</span></span><br/> <span data-ttu-id="d67b1-149">Nome del comando padre</span><span class="sxs-lookup"><span data-stu-id="d67b1-149">Parent Command name</span></span><br/> <span data-ttu-id="d67b1-150">Uno dei metodi Invoke seguenti:</span><span class="sxs-lookup"><span data-stu-id="d67b1-150">One of the following invoke methods:</span></span>
<ul>
<li><span data-ttu-id="d67b1-151">Clicca</span><span class="sxs-lookup"><span data-stu-id="d67b1-151">CLICK</span></span></li>
<li><span data-ttu-id="d67b1-152">SUGGERIMENTO tasto</span><span class="sxs-lookup"><span data-stu-id="d67b1-152">KEYTIP</span></span></li>
<li><span data-ttu-id="d67b1-153">TASTIERA</span><span class="sxs-lookup"><span data-stu-id="d67b1-153">KEYBOARD</span></span></li>
<li><span data-ttu-id="d67b1-154">TOCCO</span><span class="sxs-lookup"><span data-stu-id="d67b1-154">TOUCH</span></span></li>
</ul>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d67b1-155">Le raccolte di elementi e le caselle combinate includono l'indice dell'elemento selezionato, ma non includono valori stringa e Integer.</span><span class="sxs-lookup"><span data-stu-id="d67b1-155">Item galleries and combo boxes include the selected item index but do not include string and integer values.</span></span> <span data-ttu-id="d67b1-156">Gli Spinner non includono il valore integer.</span><span class="sxs-lookup"><span data-stu-id="d67b1-156">Spinners do not include the integer value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d67b1-157">Barra multifunzione ridotta a icona</span><span class="sxs-lookup"><span data-stu-id="d67b1-157">Ribbon minimized</span></span></td>
<td><span data-ttu-id="d67b1-158">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-158">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d67b1-159">Barra multifunzione espansa (pulsante di espansione selezionato o tocco aggiunto)</span><span class="sxs-lookup"><span data-stu-id="d67b1-159">Ribbon expanded (expand button clicked or tap pinned)</span></span></td>
<td><span data-ttu-id="d67b1-160">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-160">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d67b1-161">Modalità applicazione cambiata</span><span class="sxs-lookup"><span data-stu-id="d67b1-161">Application mode switched</span></span></td>
<td><span data-ttu-id="d67b1-162">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-162">Event verb</span></span><br/> <span data-ttu-id="d67b1-163">ID modalità (valore impostato tramite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>Semodes</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d67b1-163">Mode ID (value set through <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d67b1-164">L'applicazione è responsabile della decompressione di questo Integer per determinare le modalità impostate.</span><span class="sxs-lookup"><span data-stu-id="d67b1-164">The application is responsible for unpacking this integer to determine which modes were set.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d67b1-165">Descrizione comando visualizzata</span><span class="sxs-lookup"><span data-stu-id="d67b1-165">Tooltip displayed</span></span></td>
<td><span data-ttu-id="d67b1-166">Verbo evento</span><span class="sxs-lookup"><span data-stu-id="d67b1-166">Event verb</span></span><br/> <span data-ttu-id="d67b1-167">ID comando padre</span><span class="sxs-lookup"><span data-stu-id="d67b1-167">Parent Command ID</span></span><br/> <span data-ttu-id="d67b1-168">Nome del comando padre</span><span class="sxs-lookup"><span data-stu-id="d67b1-168">Parent Command name</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d67b1-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d67b1-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d67b1-170">Guide per gli sviluppatori di Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="d67b1-170">Windows Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)
</dt> <dt>

[<span data-ttu-id="d67b1-171">Dichiarazione di comandi e controlli con markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="d67b1-171">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="d67b1-172">Linee guida sull'esperienza utente della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="d67b1-172">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="d67b1-173">Processo di progettazione della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="d67b1-173">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

