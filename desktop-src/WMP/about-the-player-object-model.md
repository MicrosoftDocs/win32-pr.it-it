---
title: Informazioni sul modello a oggetti del lettore
description: Informazioni sul modello a oggetti del lettore
ms.assetid: 41a9cbce-b982-4377-a0ee-b0ca735954f5
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, informazioni
- modello a oggetti, informazioni
- Controllo ActiveX di Windows Media Player, modello a oggetti
- Controllo ActiveX, modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, modello a oggetti
- Windows Media Player Mobile, modello a oggetti
- Software Development Kit (SDK), modello a oggetti del controllo ActiveX di Windows Media Player
- SDK (Software Development Kit), modello a oggetti del controllo ActiveX di Windows Media Player
- documentazione, modello a oggetti del controllo ActiveX di Windows Media Player
- Oggetto Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a0ded1f25d8d08bd9e588b5384a171698d2ea2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298371"
---
# <a name="about-the-player-object-model"></a><span data-ttu-id="a4caf-114">Informazioni sul modello a oggetti del lettore</span><span class="sxs-lookup"><span data-stu-id="a4caf-114">About the Player Object Model</span></span>

<span data-ttu-id="a4caf-115">Il controllo Media Player di Microsoft Windows è un controllo ActiveX standard che utilizza la tecnologia Microsoft Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="a4caf-115">The Microsoft Windows Media Player control is a standard ActiveX control that uses Microsoft Component Object Model (COM) technology.</span></span> <span data-ttu-id="a4caf-116">La funzionalità Windows Media Player viene distillata in un set di interfacce di programmazione che segue le linee guida standard di COM.</span><span class="sxs-lookup"><span data-stu-id="a4caf-116">The Windows Media Player functionality is distilled into a set of programming interfaces that follows standard COM guidelines.</span></span> <span data-ttu-id="a4caf-117">È possibile programmare queste interfacce in una pagina Web HTML standard usando il modello a oggetti del controllo Player con Microsoft JScript o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="a4caf-117">You can program these interfaces on a standard HTML webpage using the Player control object model with Microsoft JScript or Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="a4caf-118">È inoltre possibile programmarli in interfacce utilizzando Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="a4caf-118">You can also program them in skins by using Microsoft JScript.</span></span> <span data-ttu-id="a4caf-119">Se si desidera creare un programma personalizzato che incorpora il controllo, è possibile utilizzare uno dei diversi linguaggi, tra cui Visual Basic, C++ e C#.</span><span class="sxs-lookup"><span data-stu-id="a4caf-119">If you want to create a custom program that embeds the control, you can use one of several languages, including Visual Basic, C++, and C#.</span></span>

<span data-ttu-id="a4caf-120">Il controllo ActiveX di Windows Media Player viene installato con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a4caf-120">The Windows Media Player ActiveX control is installed with Windows Media Player.</span></span> <span data-ttu-id="a4caf-121">Il controllo Player non è installato con Windows Media Player SDK e non può essere ridistribuito separatamente.</span><span class="sxs-lookup"><span data-stu-id="a4caf-121">The Player control is not installed with the Windows Media Player SDK and cannot be redistributed separately.</span></span> <span data-ttu-id="a4caf-122">Le particolari funzionalità disponibili per il codice dipendono dalla versione di Windows Media Player installata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a4caf-122">The particular features available to your code depend on which version of Windows Media Player the user has installed.</span></span> <span data-ttu-id="a4caf-123">Il [riferimento del modello a oggetti per](object-model-reference-for-scripting.md) la creazione di script e il [riferimento del modello a oggetti per C++](object-model-reference-for-c.md) includono informazioni sui requisiti di versione per ogni proprietà, metodo ed evento.</span><span class="sxs-lookup"><span data-stu-id="a4caf-123">The [Object Model Reference for Scripting](object-model-reference-for-scripting.md) and [Object Model Reference for C++](object-model-reference-for-c.md) include version requirement information for each property, method, and event.</span></span>

<span data-ttu-id="a4caf-124">Nelle sezioni seguenti vengono fornite informazioni generali sul modello a oggetti di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a4caf-124">The following sections provide overview information about the Windows Media Player object model.</span></span>



| <span data-ttu-id="a4caf-125">Sezione</span><span class="sxs-lookup"><span data-stu-id="a4caf-125">Section</span></span>                                                                                        | <span data-ttu-id="a4caf-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4caf-126">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4caf-127">Modello a oggetti del lettore per i linguaggi di scripting</span><span class="sxs-lookup"><span data-stu-id="a4caf-127">Player Object Model for Scripting Languages</span></span>](player-object-model-for-scripting-languages.md) | <span data-ttu-id="a4caf-128">In questa sezione vengono descritti gli oggetti disponibili nel modello a oggetti.</span><span class="sxs-lookup"><span data-stu-id="a4caf-128">This section describes the objects available in the object model.</span></span>                                                                                             |
| [<span data-ttu-id="a4caf-129">Informazioni sulle versioni del modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="a4caf-129">About the Object Model Versions</span></span>](about-the-object-model-versions.md)                         | <span data-ttu-id="a4caf-130">In questa sezione vengono illustrati gli elementi del modello a oggetti aggiunti in ogni versione dopo l'introduzione di Windows Media Player 7,0.</span><span class="sxs-lookup"><span data-stu-id="a4caf-130">This section details which object model items have been added in each version since the introduction of Windows Media Player 7.0.</span></span>                             |
| [<span data-ttu-id="a4caf-131">Proprietà, metodi ed eventi</span><span class="sxs-lookup"><span data-stu-id="a4caf-131">Properties, Methods, and Events</span></span>](properties--methods-and-events.md)                          | <span data-ttu-id="a4caf-132">In questa sezione vengono illustrate proprietà, metodi ed eventi.</span><span class="sxs-lookup"><span data-stu-id="a4caf-132">This section explains properties, methods, and events.</span></span>                                                                                                        |
| [<span data-ttu-id="a4caf-133">Protocolli e tipi di file supportati</span><span class="sxs-lookup"><span data-stu-id="a4caf-133">Supported Protocols and File Types</span></span>](supported-protocols-and-file-types.md)                   | <span data-ttu-id="a4caf-134">In questa sezione sono elencati i protocolli e i tipi di file supportati da Windows Media Player e il modello a oggetti del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="a4caf-134">This section lists the protocols and file types supported by Windows Media Player and the Windows Media Player control object model.</span></span>                          |
| [<span data-ttu-id="a4caf-135">Informazioni sulla libreria</span><span class="sxs-lookup"><span data-stu-id="a4caf-135">About the Library</span></span>](about-the-library.md)                                                     | <span data-ttu-id="a4caf-136">In questa sezione viene descritta la libreria Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="a4caf-136">This section describes the Windows Media Player library.</span></span>                                                                                                      |
| [<span data-ttu-id="a4caf-137">Uso di HTML con Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="a4caf-137">Using HTML with Windows Media Player</span></span>](using-html-with-windows-media-player.md)               | <span data-ttu-id="a4caf-138">In questa sezione vengono descritte le varie modalità di interazione tra Windows Media Player e HTML.</span><span class="sxs-lookup"><span data-stu-id="a4caf-138">This section describes the various ways to make Windows Media Player and HTML work together.</span></span>                                                                  |
| [<span data-ttu-id="a4caf-139">Incorporamento del controllo Media Player Windows</span><span class="sxs-lookup"><span data-stu-id="a4caf-139">Embedding the Windows Media Player Control</span></span>](embedding-the-windows-media-player-control.md)   | <span data-ttu-id="a4caf-140">In questa sezione vengono descritti i vari modi per incorporare il controllo Windows Media Player in Microsoft Office documenti e in programmi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="a4caf-140">This section describes the various ways to embed the Windows Media Player control in Microsoft Office documents and in custom programs.</span></span>                       |
| [<span data-ttu-id="a4caf-141">Informazioni sulla sincronizzazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="a4caf-141">About Device Synchronization</span></span>](about-device-synchronization.md)                               | <span data-ttu-id="a4caf-142">In questa sezione vengono descritte le funzionalità fornite dal controllo Windows Media Player 10 o versione successiva per il trasferimento di contenuti multimediali digitali a dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="a4caf-142">This section describes the functionality provided by the Windows Media Player 10 or later control for transferring digital media content to portable devices.</span></span> |
| [<span data-ttu-id="a4caf-143">Informazioni sulla masterizzazione di CD</span><span class="sxs-lookup"><span data-stu-id="a4caf-143">About CD Burning</span></span>](about-cd-burning.md)                                                       | <span data-ttu-id="a4caf-144">In questa sezione vengono descritte le funzionalità fornite dal controllo Media Player Windows per la creazione di CDs.</span><span class="sxs-lookup"><span data-stu-id="a4caf-144">This section describes the functionality provided by the Windows Media Player control for creating CDs.</span></span>                                                       |
| [<span data-ttu-id="a4caf-145">Informazioni sul ripping del CD</span><span class="sxs-lookup"><span data-stu-id="a4caf-145">About CD Ripping</span></span>](about-cd-ripping.md)                                                       | <span data-ttu-id="a4caf-146">In questa sezione vengono descritte le funzionalità fornite dal controllo Media Player di Windows per la copia di tracce da CD audio nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a4caf-146">This section describes the functionality provided by the Windows Media Player control for copying tracks from audio CDs to the user's computer.</span></span>               |
| [<span data-ttu-id="a4caf-147">Informazioni sul monitoraggio delle cartelle</span><span class="sxs-lookup"><span data-stu-id="a4caf-147">About Folder Monitoring</span></span>](about-folder-monitoring.md)                                         | <span data-ttu-id="a4caf-148">In questa sezione vengono descritte le funzionalità fornite dal controllo Media Player Windows per il controllo dei processi di monitoraggio delle cartelle del lettore.</span><span class="sxs-lookup"><span data-stu-id="a4caf-148">This section describes the functionality provided by the Windows Media Player control for controlling the Player's folder monitoring processes.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="a4caf-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4caf-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4caf-150">**Modello a oggetti di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="a4caf-150">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




