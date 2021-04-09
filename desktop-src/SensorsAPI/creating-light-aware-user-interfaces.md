---
description: Questa sezione illustra l'uso dei dati del sensore luce di ambiente e il modo in cui le funzionalità dell'interfaccia utente e il contenuto del programma possono essere ottimizzati per molte condizioni di illuminazione.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Creazione di interfacce utente Light-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968005"
---
# <a name="creating-light-aware-user-interfaces"></a><span data-ttu-id="8805c-103">Creazione di interfacce utente Light-Aware</span><span class="sxs-lookup"><span data-stu-id="8805c-103">Creating Light-Aware User Interfaces</span></span>

<span data-ttu-id="8805c-104">Questa sezione illustra l'uso dei dati del sensore luce di ambiente e il modo in cui le funzionalità dell'interfaccia utente e il contenuto del programma possono essere ottimizzati per molte condizioni di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="8805c-104">This section covers the use of ambient light sensor data, and how user interface features and program content can be optimized for many lighting conditions.</span></span>

<span data-ttu-id="8805c-105">I sensori di ambiente chiaro espongono i dati che possono essere usati per determinare i vari aspetti delle condizioni di illuminazione in cui si trova il sensore.</span><span class="sxs-lookup"><span data-stu-id="8805c-105">Ambient light sensors expose data that can be used to determine various aspects of the lighting conditions where the sensor is located.</span></span> <span data-ttu-id="8805c-106">I sensori di luce di ambiente possono esporre la luminosità complessiva di un ambiente (illuminazione) e di altri aspetti della luce circostante, ad esempio la cromaticità o la temperatura dei colori.</span><span class="sxs-lookup"><span data-stu-id="8805c-106">Ambient light sensors can expose the overall brightness of an environment (illuminance) and other aspects of the surrounding light, such as chromaticity or color temperature.</span></span>

<span data-ttu-id="8805c-107">I computer possono essere più utili in diversi modi quando il sistema risponde alle condizioni di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="8805c-107">Computers can be more useful in several ways when the system is responsive to lighting conditions.</span></span> <span data-ttu-id="8805c-108">Questi includono il controllo della luminosità dello schermo del computer (una nuova funzionalità completamente supportata in Windows 7), la regolazione automatica del livello di illuminazione delle tastiere illuminate e anche il controllo della luminosità per altre luci, ad esempio l'illuminazione dei pulsanti, le luci delle attività e così via.</span><span class="sxs-lookup"><span data-stu-id="8805c-108">These include controlling the brightness of the computer display (a new, fully supported feature in Windows 7), automatically adjusting the lighting level of illuminated keyboards, and even brightness control for other lights (such as button illumination, activity lights, and so on).</span></span>

<span data-ttu-id="8805c-109">I programmi per gli utenti finali possono trarre vantaggio anche dai sensori leggeri.</span><span class="sxs-lookup"><span data-stu-id="8805c-109">End-user programs can also benefit from light sensors.</span></span> <span data-ttu-id="8805c-110">I programmi possono applicare un tema appropriato per una particolare condizione di illuminazione, ad esempio un tema esterno specifico e un tema interno.</span><span class="sxs-lookup"><span data-stu-id="8805c-110">Programs can apply a theme that is appropriate for a particular lighting condition, such as a specific outdoor theme and indoor theme.</span></span> <span data-ttu-id="8805c-111">Forse l'aspetto più importante dell'integrazione dei sensori di luce con i programmi è la leggibilità e le ottimizzazioni di leggibilità basate sulle condizioni di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="8805c-111">Perhaps the most important aspect of light sensor integration with programs is readability and legibility optimizations that are based on lighting conditions.</span></span>

<span data-ttu-id="8805c-112">L'API Sensor consente di creare programmi di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="8805c-112">The Sensor API enables you to create such programs.</span></span> <span data-ttu-id="8805c-113">Si consideri lo scenario seguente.</span><span class="sxs-lookup"><span data-stu-id="8805c-113">Consider the following scenario.</span></span>

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a><span data-ttu-id="8805c-114">Scenario: uso del computer portatile per passare a un ristorante</span><span class="sxs-lookup"><span data-stu-id="8805c-114">Scenario: Using your Laptop to Navigate to a Restaurant</span></span>

<span data-ttu-id="8805c-115">Si supponga di voler usare il computer per accedere a un nuovo ristorante.</span><span class="sxs-lookup"><span data-stu-id="8805c-115">Suppose you want to use your computer to help you navigate to a new restaurant.</span></span> <span data-ttu-id="8805c-116">Si inizia a casa, si cerca l'indirizzo del ristorante e si pianifica il percorso.</span><span class="sxs-lookup"><span data-stu-id="8805c-116">You start out in your house, looking up the address of the restaurant and planning your route.</span></span> <span data-ttu-id="8805c-117">Lo screenshot seguente mostra in che modo il programma di navigazione potrebbe ottimizzare l'interfaccia utente per visualizzare informazioni dettagliate sulle condizioni di illuminazione interna.</span><span class="sxs-lookup"><span data-stu-id="8805c-117">The following screen shot shows how your navigation program could optimize its UI to show detailed information in indoor lighting conditions.</span></span>

![interfaccia utente progettata per l'illuminazione interna.](images/nav-normal.png)

<span data-ttu-id="8805c-119">Quando si esce dalla propria auto, viene visualizzato il sole diretto, che rende difficile la lettura dello schermo del portatile.</span><span class="sxs-lookup"><span data-stu-id="8805c-119">When you go outside to your car, you encounter direct sunlight, which makes the laptop's screen difficult to read.</span></span> <span data-ttu-id="8805c-120">Lo screenshot seguente illustra il modo in cui il programma potrebbe modificare l'interfaccia utente per ottimizzare la leggibilità e la leggibilità con la luce diretta.</span><span class="sxs-lookup"><span data-stu-id="8805c-120">The following screen shot shows how your program could alter its UI to maximize legibility/readability in direct light.</span></span> <span data-ttu-id="8805c-121">In questa visualizzazione, gran parte del dettaglio è stata omessa e il contrasto è ingrandito.</span><span class="sxs-lookup"><span data-stu-id="8805c-121">In this view, much of the detail has been omitted and contrast is maximized.</span></span>

![interfaccia utente progettata per le condizioni di illuminazione diretta.](images/nav-contrast.png)

<span data-ttu-id="8805c-123">Man mano che ci si avvicina al ristorante, la sera si avvicina e diventa scura al di fuori.</span><span class="sxs-lookup"><span data-stu-id="8805c-123">As you get closer to the restaurant, evening approaches and it gets dark outside.</span></span> <span data-ttu-id="8805c-124">Nello screenshot seguente, l'interfaccia utente per il programma di navigazione è stata ottimizzata per la visualizzazione di bassa luminosità.</span><span class="sxs-lookup"><span data-stu-id="8805c-124">In the following screen shot, the UI for the navigation program has been optimized for low-light viewing.</span></span> <span data-ttu-id="8805c-125">Usando i colori più scuri nel suo complesso, questa interfaccia utente è facile da guardare nell'auto scura.</span><span class="sxs-lookup"><span data-stu-id="8805c-125">By using darker colors overall, this UI is easy to glance at in the dark car.</span></span>

![interfaccia utente progettata per la visualizzazione a bassa luminosità.](images/nav-lowlight.png)

<span data-ttu-id="8805c-127">Nella parte restante di questa sezione si esamineranno alcune operazioni che è possibile eseguire per ottimizzare i programmi per diverse condizioni di illuminazione e come usare l'API del sensore per abilitare l'interfaccia utente che supporta la luce.</span><span class="sxs-lookup"><span data-stu-id="8805c-127">In the remainder of this section, you will explore some things that you can do to optimize your programs for various lighting conditions and how you can use the Sensor API to help enable light-aware UI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8805c-128">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8805c-128">In This Section</span></span>

-   [<span data-ttu-id="8805c-129">Nozioni fondamentali sulle interfacce utente Light-Aware</span><span class="sxs-lookup"><span data-stu-id="8805c-129">Fundamentals of Light-Aware User Interfaces</span></span>](fundamentals-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="8805c-130">Esempi di interfacce utente Light-Aware</span><span class="sxs-lookup"><span data-stu-id="8805c-130">Examples of Light-Aware User Interfaces</span></span>](examples-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="8805c-131">Ottimizzazione dell'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="8805c-131">Optimizing the User Experience</span></span>](optimizing-the-user-experience.md)
-   [<span data-ttu-id="8805c-132">Informazioni e interpretazione dei valori Lux</span><span class="sxs-lookup"><span data-stu-id="8805c-132">Understanding and Interpreting Lux Values</span></span>](understanding-and-interpreting-lux-values.md)
-   [<span data-ttu-id="8805c-133">Uso dei dati del sensore chiaro</span><span class="sxs-lookup"><span data-stu-id="8805c-133">Using Light Sensor Data</span></span>](handling-data-from-multiple-light-sensors.md)

 

 



