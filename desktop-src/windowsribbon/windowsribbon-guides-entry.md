---
title: Guide per gli sviluppatori di Windows Ribbon Framework
description: Gli argomenti contenuti in questa sezione descrivono aspetti specifici del Framework della barra multifunzione di Windows.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Barra multifunzione di Windows, Framework
- Barra multifunzione, Framework
- Barra multifunzione di Windows, guide per sviluppatori
- Barra multifunzione, guide per sviluppatori
- Guide per sviluppatori per la barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118266"
---
# <a name="windows-ribbon-framework-developer-guides"></a><span data-ttu-id="1398c-108">Guide per gli sviluppatori di Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="1398c-108">Windows Ribbon Framework Developer Guides</span></span>

<span data-ttu-id="1398c-109">Gli argomenti contenuti in questa sezione descrivono aspetti specifici del Framework della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="1398c-109">The topics contained in this section describe specific aspects of the Windows Ribbon framework.</span></span>

## <a name="basics"></a><span data-ttu-id="1398c-110">Nozioni di base</span><span class="sxs-lookup"><span data-stu-id="1398c-110">Basics</span></span>

[<span data-ttu-id="1398c-111">Creazione di un'applicazione Ribbon</span><span class="sxs-lookup"><span data-stu-id="1398c-111">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)

<span data-ttu-id="1398c-112">Affinché il Framework della barra multifunzione di Windows utilizzi il file di markup della barra multifunzione, il file di markup deve essere compilato in un file di risorse in formato binario.</span><span class="sxs-lookup"><span data-stu-id="1398c-112">For the Windows Ribbon framework to consume the Ribbon markup file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="1398c-113">Un compilatore di markup della barra multifunzione dedicato, il compilatore di comandi dell'interfaccia utente (UICC), è incluso con Microsoft Windows Software Development Kit (SDK) (7,0 o versione successiva) a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="1398c-113">A dedicated Ribbon markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="1398c-114">Oltre a compilare la versione binaria del markup della barra multifunzione, UICC genera un file di intestazione di definizione ID (con estensione h) che espone tutti gli elementi di markup all'applicazione host della barra multifunzione e un file di risorse (RC) usato per collegare le risorse di tipo immagine e stringa all'applicazione host in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="1398c-114">In addition to compiling the binary version of the Ribbon markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="1398c-115">Migrazione al framework della barra multifunzione di Windows</span><span class="sxs-lookup"><span data-stu-id="1398c-115">Migrating to the Windows Ribbon Framework</span></span>](ribbon-migration.md)

<span data-ttu-id="1398c-116">È possibile eseguire la migrazione di un'applicazione che si basa sui menu tradizionali, sulle barre degli strumenti e sulle finestre di dialogo nell'interfaccia utente avanzata, dinamica e basata sul contesto del sistema di comandi del Framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="1398c-116">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven user interface (UI) of the Ribbon framework Command system.</span></span> <span data-ttu-id="1398c-117">Si tratta di un modo semplice ed efficace per modernizzare e rivitalizzare l'applicazione, migliorando al tempo stesso l'accessibilità, l'usabilità e l'individuabilità delle relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1398c-117">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

[<span data-ttu-id="1398c-118">Informazioni sui comandi e sui controlli</span><span class="sxs-lookup"><span data-stu-id="1398c-118">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)

<span data-ttu-id="1398c-119">La separazione della logica dalla presentazione è la filosofia di progettazione che ispira il sistema di presentazione dei comandi del Framework della barra multifunzione, un sistema basato su uno schema progettuale in cui funzionalità e comportamento vengono implementate indipendentemente dai controlli che espongono questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1398c-119">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

## <a name="user-interface"></a><span data-ttu-id="1398c-120">Interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1398c-120">User Interface</span></span>

[<span data-ttu-id="1398c-121">Specifica delle risorse dell'immagine della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="1398c-121">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)

<span data-ttu-id="1398c-122">Poiché è un sistema di presentazione dei comandi avanzato, il Framework della barra multifunzione è progettato per supportare ampiamente le risorse dell'immagine nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="1398c-122">As a rich command presentation system, the Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="1398c-123">Tutte le risorse immagine sono dichiarate in [markup della barra multifunzione](windowsribbon-schema.md) o eseguite da un'applicazione host della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="1398c-123">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="1398c-124">Per Windows 8 e versioni successive, il Framework della barra multifunzione supporta i formati grafici seguenti: file di bitmap (BMP) a 32 bit ARGB (BMP) e file Portable Network Graphics (PNG) con trasparenza.</span><span class="sxs-lookup"><span data-stu-id="1398c-124">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="1398c-125">Per Windows 7 e versioni precedenti, le risorse di immagine devono essere conformi al formato di grafica BMP standard usato in Windows.</span><span class="sxs-lookup"><span data-stu-id="1398c-125">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

[<span data-ttu-id="1398c-126">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="1398c-126">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)

<span data-ttu-id="1398c-127">I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione e basati su una combinazione di comportamenti predefiniti e modelli di layout (definiti dal Framework e personalizzati) come dichiarati nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="1398c-127">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="1398c-128">Queste regole definiscono i comportamenti del layout adattivo del Framework della barra multifunzione che influenzano il modo in cui i controlli della barra dei comandi si adattano a diverse dimensioni della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1398c-128">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

[<span data-ttu-id="1398c-129">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="1398c-129">Working with Galleries</span></span>](ribbon-controls-galleries.md)

<span data-ttu-id="1398c-130">Il Framework della barra multifunzione offre agli sviluppatori un modello affidabile e coerente per la gestione di contenuto dinamico in diversi controlli basati sulle raccolte.</span><span class="sxs-lookup"><span data-stu-id="1398c-130">The Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="1398c-131">Grazie all'adattamento e alla riconfigurazione dell'interfaccia utente della barra multifunzione, questi controlli dinamici consentono al Framework di rispondere all'interazione dell'utente sia nell'applicazione host che nella barra multifunzione e offrono la flessibilità necessaria per gestire diversi ambienti di Runtime.</span><span class="sxs-lookup"><span data-stu-id="1398c-131">By adapting and reconfiguring the Ribbon user interface (UI), these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

[<span data-ttu-id="1398c-132">Visualizzazione di schede contestuali</span><span class="sxs-lookup"><span data-stu-id="1398c-132">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)

<span data-ttu-id="1398c-133">In un'applicazione Ribbon Framework, una scheda contestuale è un controllo struttura a [schede](windowsribbon-controls-tab.md) nascosto visualizzato nella scheda quando un oggetto nell'area di lavoro dell'applicazione, ad esempio un'immagine, viene selezionato o evidenziato.</span><span class="sxs-lookup"><span data-stu-id="1398c-133">In a Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

[<span data-ttu-id="1398c-134">Riconfigurazione della barra multifunzione con le modalità applicazione</span><span class="sxs-lookup"><span data-stu-id="1398c-134">Reconfiguring the Ribbon with Application Modes</span></span>](ribbon-applicationmodes.md)

<span data-ttu-id="1398c-135">Il Framework della barra multifunzione supporta la riconfigurazione dinamica e l'esposizione degli elementi principali dell'interfaccia utente della barra multifunzione in fase di esecuzione, in base allo stato dell'applicazione (noto anche come contesto).</span><span class="sxs-lookup"><span data-stu-id="1398c-135">The Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon user interface (UI) at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="1398c-136">Dichiarati e associati a elementi specifici nel markup, i vari stati supportati da un'applicazione sono definiti modalità applicazione.</span><span class="sxs-lookup"><span data-stu-id="1398c-136">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

[<span data-ttu-id="1398c-137">Personalizzazione dei colori della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="1398c-137">Customizing Ribbon Colors</span></span>](ribbon-color.md)

<span data-ttu-id="1398c-138">Il Framework della barra multifunzione espone un set di proprietà cromatiche che consentono a un'applicazione di personalizzare l'aspetto di diversi elementi dell'interfaccia utente della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1398c-138">The Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon user interface (UI) elements at run time.</span></span>

[<span data-ttu-id="1398c-139">Visualizzazione della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="1398c-139">Displaying the Ribbon</span></span>](ribbon-visibility.md)

<span data-ttu-id="1398c-140">Il Framework della barra multifunzione espone un set di proprietà che consentono a un'applicazione di specificare la modalità di visualizzazione dell'interfaccia utente della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1398c-140">The Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon user interface (UI) is displayed at run time.</span></span>

## <a name="management"></a><span data-ttu-id="1398c-141">Gestione</span><span class="sxs-lookup"><span data-stu-id="1398c-141">Management</span></span>

[<span data-ttu-id="1398c-142">Mantenimento dello stato della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="1398c-142">Persisting Ribbon State</span></span>](ribbon-statepersistence.md)

<span data-ttu-id="1398c-143">Windows Ribon Framework (barra multifunzione) offre la possibilità di mantenere lo stato di un'ampia gamma di impostazioni utente e preferenze tra le sessioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1398c-143">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

[<span data-ttu-id="1398c-144">Ascolto degli eventi della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="1398c-144">Listening for Ribbon Events</span></span>](listening-for-ribbon-events.md)

<span data-ttu-id="1398c-145">Il Framework della barra multifunzione usa l'infrastruttura di [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) per consentire agli sviluppatori di apprendere il modo in cui gli utenti interagiscono con la barra multifunzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1398c-145">The Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="markup-compiler"></a><span data-ttu-id="1398c-146">Compilatore di markup</span><span class="sxs-lookup"><span data-stu-id="1398c-146">Markup Compiler</span></span>

[<span data-ttu-id="1398c-147">Compilazione del markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="1398c-147">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)

<span data-ttu-id="1398c-148">Affinché il Framework della barra multifunzione utilizzi il file di [markup della barra multifunzione](windowsribbon-schema.md) , il file di markup deve essere compilato in un file di risorse in formato binario.</span><span class="sxs-lookup"><span data-stu-id="1398c-148">For the Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="1398c-149">Un compilatore di markup dedicato, il compilatore di comandi dell'interfaccia utente (UICC), è incluso con Microsoft Windows Software Development Kit (SDK) (7,0 o versione successiva) a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="1398c-149">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Microsoft Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="1398c-150">Oltre a compilare la versione binaria del markup, UICC genera un file di intestazione di definizione ID (con estensione h) che espone tutti gli elementi di markup all'applicazione host della barra multifunzione e un file di risorse (RC) usato per collegare le risorse di tipo immagine e stringa all'applicazione host in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="1398c-150">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

[<span data-ttu-id="1398c-151">Informazioni sui messaggi del compilatore di markup</span><span class="sxs-lookup"><span data-stu-id="1398c-151">Understanding Markup Compiler Messages</span></span>](windowsribbon-compilationerrors.md)

<span data-ttu-id="1398c-152">Il compilatore di markup di Windows Ribbon Framework (barra multifunzione), il compilatore di comandi dell'interfaccia utente (UICC.exe), convalida il markup della barra multifunzione rispetto allo schema della barra multifunzione e un set aggiuntivo di regole definito dal framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="1398c-152">The Windows Ribbon framework (Ribbon) markup compiler, UI Command Compiler (UICC.exe), validates the Ribbon markup against both the Ribbon schema and an additional set of rules defined by the Ribbon framework.</span></span>

 

 