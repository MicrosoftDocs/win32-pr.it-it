---
description: Per ulteriori informazioni sul diagramma seguente, vedere la legenda del diagramma delle relazioni tra entità.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Gruppo di tabelle Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968396"
---
# <a name="core-tables-group"></a><span data-ttu-id="270b5-103">Gruppo di tabelle Core</span><span class="sxs-lookup"><span data-stu-id="270b5-103">Core Tables Group</span></span>

<span data-ttu-id="270b5-104">Per ulteriori informazioni sul diagramma seguente, vedere la [legenda del diagramma delle relazioni tra entità](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="270b5-104">For more information about the following diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

![gruppo di tabelle Core](images/core.png)

<span data-ttu-id="270b5-106">Il gruppo principale è costituito da tabelle che descrivono le funzionalità e i componenti fondamentali dell'applicazione e del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="270b5-106">The core group consists of tables describing the fundamental features and components of the application and the installer package.</span></span> <span data-ttu-id="270b5-107">Gli sviluppatori di pacchetti di installazione dovrebbero quindi considerare come popolare queste tabelle prima perché l'organizzazione di gran parte del database diventerà evidente dal contenuto di questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="270b5-107">Developers of install packages should therefore consider how to populate these tables first because the organization of much of the database will become apparent from the content of this group.</span></span>

-   <span data-ttu-id="270b5-108">La [tabella Feature](feature-table.md) elenca tutte le funzionalità appartenenti all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="270b5-108">The [Feature table](feature-table.md) lists all features belonging to the application.</span></span>
-   <span data-ttu-id="270b5-109">La [tabella della condizione](condition-table.md) contiene le espressioni condizionali che determinano se verrà installata una particolare funzionalità o meno.</span><span class="sxs-lookup"><span data-stu-id="270b5-109">The [Condition table](condition-table.md) contains the conditional expressions that determine whether or not a particular feature will be installed.</span></span>
-   <span data-ttu-id="270b5-110">Nella [tabella FeatureComponents](featurecomponents-table.md) vengono descritti i componenti appartenenti a ciascuna funzionalità.</span><span class="sxs-lookup"><span data-stu-id="270b5-110">The [FeatureComponents table](featurecomponents-table.md) describes which components belong to each feature.</span></span>
-   <span data-ttu-id="270b5-111">La [tabella Component](component-table.md) elenca tutti i componenti appartenenti all'installazione.</span><span class="sxs-lookup"><span data-stu-id="270b5-111">The [Component table](component-table.md) lists all components belonging to the installation.</span></span>
-   <span data-ttu-id="270b5-112">Nella [tabella directory](directory-table.md) sono elencate le directory necessarie durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="270b5-112">The [Directory table](directory-table.md) lists the directories that are needed during the installation.</span></span> <span data-ttu-id="270b5-113">Poiché ogni componente deve essere associato a una sola directory, la tabella dei componenti è strettamente correlata a questa tabella e include una chiave esterna per la tabella di directory.</span><span class="sxs-lookup"><span data-stu-id="270b5-113">Because each component must be associated with one and only one directory, the Component table is closely related to this table and has an external key to the Directory table.</span></span>
-   <span data-ttu-id="270b5-114">Nella [tabella PublishComponent](publishcomponent-table.md) sono elencate le funzionalità e i componenti pubblicati per l'utilizzo da parte di altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="270b5-114">The [PublishComponent table](publishcomponent-table.md) lists the features and components that are published for use by other applications.</span></span> <span data-ttu-id="270b5-115">I [componenti e le funzionalità](components-and-features.md) sono i due tipi di annunci di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="270b5-115">[Components and Features](components-and-features.md) are the two types of feature advertisement.</span></span>
-   <span data-ttu-id="270b5-116">La [tabella MsiAssembly](msiassembly-table.md) specifica le impostazioni Windows Installer per gli assembly di Common Language Runtime di .NET Framework e Win32.</span><span class="sxs-lookup"><span data-stu-id="270b5-116">The [MsiAssembly table](msiassembly-table.md) specifies Windows Installer settings for .NET Framework common language runtime assemblies and Win32 assemblies.</span></span>
-   <span data-ttu-id="270b5-117">La [tabella MsiAssemblyName](msiassemblyname-table.md) specifica lo schema per gli elementi di un nome di assembly cache forte per un Common Language Runtime o un assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="270b5-117">The [MsiAssemblyName table](msiassemblyname-table.md) specifies the schema for the elements of a strong assembly cache name for a common language runtime or Win32 assembly.</span></span>
-   <span data-ttu-id="270b5-118">La [tabella ComPlus](complus-table.md) contiene le informazioni necessarie per installare le applicazioni com+.</span><span class="sxs-lookup"><span data-stu-id="270b5-118">The [Complus table](complus-table.md) contains information needed to install COM+ applications.</span></span>
-   <span data-ttu-id="270b5-119">La [tabella IsolatedComponent](isolatedcomponent-table.md) associa il componente specificato nella \_ colonna applicazione componente (in genere un file con estensione exe) con il componente specificato nella \_ colonna condivisa componente (in genere una DLL condivisa).</span><span class="sxs-lookup"><span data-stu-id="270b5-119">The [IsolatedComponent table](isolatedcomponent-table.md) associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span>
-   <span data-ttu-id="270b5-120">La [tabella di aggiornamento](upgrade-table.md) contiene le informazioni necessarie durante gli [aggiornamenti principali](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="270b5-120">The [Upgrade table](upgrade-table.md) contains information required during [major upgrades](major-upgrades.md).</span></span>

 

 



