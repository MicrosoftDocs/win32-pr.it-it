---
description: In modo che i sottoscrittori possano trovare una classe di evento e sottoscriverla, le classi di evento devono essere registrate nel catalogo COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registrazione di una classe di evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748290"
---
# <a name="registering-an-event-class"></a><span data-ttu-id="545ab-103">Registrazione di una classe di evento</span><span class="sxs-lookup"><span data-stu-id="545ab-103">Registering an Event Class</span></span>

<span data-ttu-id="545ab-104">In modo che i sottoscrittori possano trovare una classe di evento e sottoscriverla, le classi di evento devono essere registrate nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="545ab-104">So that subscribers can find an event class and subscribe to it, event classes must be registered in the COM+ catalog.</span></span> <span data-ttu-id="545ab-105">COM+ richiede una libreria dei tipi che descrive le interfacce e i metodi degli eventi in modo che sia possibile trovare una corrispondenza corretta e connettere i sottoscrittori e i Publisher.</span><span class="sxs-lookup"><span data-stu-id="545ab-105">COM+ requires a type library that describes the event interfaces and methods so that it can properly match and connect subscribers and publishers.</span></span> <span data-ttu-id="545ab-106">La libreria dei tipi deve risiedere in o essere accompagnata da una DLL con registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="545ab-106">The type library must reside in or be accompanied by a self-registering DLL.</span></span>

<span data-ttu-id="545ab-107">È possibile utilizzare lo strumento di amministrazione Servizi componenti o le funzioni amministrative COM+ per registrare una classe di evento nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="545ab-107">You can use the Component Services administrative tool or the COM+ Administrative functions to register an event class in the COM+ catalog.</span></span>

<span data-ttu-id="545ab-108">**Per registrare una classe di evento con lo strumento di amministrazione Servizi componenti**</span><span class="sxs-lookup"><span data-stu-id="545ab-108">**To register an event class with the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="545ab-109">Creare una nuova applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="545ab-109">Create a new COM+ application.</span></span>

2.  <span data-ttu-id="545ab-110">Aprire la cartella dell'applicazione e selezionare **componenti**.</span><span class="sxs-lookup"><span data-stu-id="545ab-110">Open the application folder and select **Components**.</span></span>

3.  <span data-ttu-id="545ab-111">Scegliere **Nuovo** dal menu **Azione**.</span><span class="sxs-lookup"><span data-stu-id="545ab-111">On the **Action** menu, click **New**.</span></span> <span data-ttu-id="545ab-112">È anche possibile selezionare la cartella **componenti** , fare clic con il pulsante destro del mouse, scegliere **nuovo**, quindi fare clic su **componente**.</span><span class="sxs-lookup"><span data-stu-id="545ab-112">(You can also select the **Components** folder, right-click, point to **New**, and then click **Component**.)</span></span>

4.  <span data-ttu-id="545ab-113">Fare clic su **installa nuove classi di evento**.</span><span class="sxs-lookup"><span data-stu-id="545ab-113">Click **Install new event class(es)**.</span></span>

5.  <span data-ttu-id="545ab-114">Immettere il percorso della DLL del componente della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="545ab-114">Enter the path to the event class component DLL.</span></span>

6.  <span data-ttu-id="545ab-115">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="545ab-115">Click **OK**.</span></span>

<span data-ttu-id="545ab-116">La classe di evento è registrata nel catalogo COM+ e può essere individuata dai sottoscrittori interessati a ottenere le informazioni fornite dalla classe di evento.</span><span class="sxs-lookup"><span data-stu-id="545ab-116">The event class is registered in the COM+ catalog and can be located by subscribers interested in obtaining the information provided by the event class.</span></span> <span data-ttu-id="545ab-117">Per informazioni su come registrare la classe di evento usando le interfacce amministrative COM+, vedere [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span><span class="sxs-lookup"><span data-stu-id="545ab-117">For information about how to register the event class by using the COM+ administrative interfaces, see [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="545ab-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="545ab-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="545ab-119">Registrazione di una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="545ab-119">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 



