---
description: Nell'esempio seguente viene illustrato come avviare un file HTML al termine di un'installazione.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232435"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a><span data-ttu-id="f312b-103">Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione</span><span class="sxs-lookup"><span data-stu-id="f312b-103">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>

<span data-ttu-id="f312b-104">Nell'esempio seguente viene illustrato come avviare un file HTML al termine di un'installazione.</span><span class="sxs-lookup"><span data-stu-id="f312b-104">The following example illustrates how to launch an HTML file at the end of an installation.</span></span> <span data-ttu-id="f312b-105">Il programma di installazione installa il componente che contiene il file e quindi pubblica un evento di controllo alla fine dell'installazione per eseguire un'azione personalizzata che apre il file.</span><span class="sxs-lookup"><span data-stu-id="f312b-105">The Installer installs the component that contains the file, and then publishes a control event at the end of the installation to run a custom action that opens the file.</span></span> <span data-ttu-id="f312b-106">Questo approccio può essere usato per avviare un'esercitazione della Guida alla fine della prima installazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f312b-106">This approach may be used to launch a help tutorial at the end of the first installation of an application.</span></span>

<span data-ttu-id="f312b-107">L'esempio deve soddisfare le specifiche seguenti.</span><span class="sxs-lookup"><span data-stu-id="f312b-107">The sample must meet the following specifications.</span></span>

-   <span data-ttu-id="f312b-108">Il programma di installazione esegue l'azione personalizzata solo se viene usato il livello di [*interfaccia utente completo*](f-gly.md) per installare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f312b-108">The Installer executes the custom action only if the [*full UI*](f-gly.md) level is used to install an application.</span></span>
-   <span data-ttu-id="f312b-109">Il programma di installazione esegue l'azione personalizzata solo se il componente che contiene il file HTML è installato per l'esecuzione locale nel computer.</span><span class="sxs-lookup"><span data-stu-id="f312b-109">The Installer executes the custom action only if the component that contains the HTML file is installed to run locally on the computer.</span></span>
-   <span data-ttu-id="f312b-110">L'azione personalizzata viene eseguita solo alla prima installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f312b-110">The custom action only runs on the first installation of the application.</span></span>
-   <span data-ttu-id="f312b-111">Se l'azione personalizzata ha esito negativo, l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="f312b-111">The installation does not fail if the custom action fails.</span></span>

<span data-ttu-id="f312b-112">Nell'esempio è incluso un ipotetico componente denominato tutorial che controlla almeno una risorsa, un file denominato tutorial.htm.</span><span class="sxs-lookup"><span data-stu-id="f312b-112">The sample includes a hypothetical component named Tutorial that controls at least one resource, a file named tutorial.htm.</span></span> <span data-ttu-id="f312b-113">L'identificatore per questo file nella colonna file della tabella file è tutorial.</span><span class="sxs-lookup"><span data-stu-id="f312b-113">The identifier for this file in the File column of the File table is Tutorial.</span></span> <span data-ttu-id="f312b-114">Nella discussione seguente si presuppone che siano già state create le risorse necessarie per l'esercitazione e che siano state apportate tutte le voci necessarie nelle tabelle [feature](feature-table.md), [Component](component-table.md), [file](file-table.md), [directory](directory-table.md)e [FeatureComponents](featurecomponents-table.md) per installare questo componente.</span><span class="sxs-lookup"><span data-stu-id="f312b-114">The following discussion assumes that you have already created the resources required by Tutorial, and have made all the necessary entries in the [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md), and [FeatureComponents](featurecomponents-table.md) tables to install this component.</span></span> <span data-ttu-id="f312b-115">Per ulteriori informazioni, vedere [un esempio di installazione](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="f312b-115">For more information, see [An Installation Example](an-installation-example.md).</span></span>

<span data-ttu-id="f312b-116">Negli argomenti seguenti sono contenute informazioni su come creare azioni personalizzate obbligatorie e aggiungerle a un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="f312b-116">The following topics contain information about how to create required custom actions and add them to an installation package.</span></span>

-   [<span data-ttu-id="f312b-117">Creazione dell'azione personalizzata di avvio</span><span class="sxs-lookup"><span data-stu-id="f312b-117">Authoring the Launch Custom Action</span></span>](authoring-the-launch-custom-action.md)
-   [<span data-ttu-id="f312b-118">Aggiunta dell'avvio alle tabelle CustomAction e binarie</span><span class="sxs-lookup"><span data-stu-id="f312b-118">Adding Launch to the CustomAction and Binary Tables</span></span>](adding-launch-to-the-customaction-and-binary-tables.md)
-   [<span data-ttu-id="f312b-119">Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio</span><span class="sxs-lookup"><span data-stu-id="f312b-119">Adding a Control Event at the End of the Installation to Run Launch</span></span>](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



