---
title: Aggiornamento dalla versione precedente
description: Aggiornamento dalla versione precedente
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297867"
---
# <a name="updating-from-previous-version"></a><span data-ttu-id="7f0ad-103">Aggiornamento dalla versione precedente</span><span class="sxs-lookup"><span data-stu-id="7f0ad-103">Updating from Previous Version</span></span>

<span data-ttu-id="7f0ad-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7f0ad-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7f0ad-105">Le applicazioni compilate e compilate con la versione 1,5 precedente di Microsoft Agent devono essere eseguite senza modifiche nella nuova versione 2,0.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-105">Applications built and compiled with the previous 1.5 version of Microsoft Agent should run without modification under the new 2.0 version.</span></span> <span data-ttu-id="7f0ad-106">La proprietà [**connessa**](connected-property.md) non può più essere impostata su **false**; alcune proprietà dell'oggetto SpeechInput che sono state sostituite sono ancora disponibili, ma non trasformano più alcun valore e il server non genera più gli eventi di [**riavvio**](https://www.bing.com/search?q=**Restart**) e [**arresto**](https://www.bing.com/search?q=**Shutdown**) .</span><span class="sxs-lookup"><span data-stu-id="7f0ad-106">The [**Connected**](connected-property.md) property can no longer be set to **False**; certain properties of the SpeechInput object that have been replaced still exist, but no longer turn any values, and the server no longer fires the [**Restart**](https://www.bing.com/search?q=**Restart**) and [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) events.</span></span>

<span data-ttu-id="7f0ad-107">Tuttavia, se si aggiornano le applicazioni per l'utilizzo del controllo Agent 2,0, potrebbe essere necessario modificare il codice.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-107">However, if you update your applications to use the Agent 2.0 control, you may have to modify your code.</span></span> <span data-ttu-id="7f0ad-108">Se è stata installata la versione 2,0 di Microsoft Agent e si carica un progetto Visual Basic usare la versione precedente del controllo agente, Visual Basic include un'opzione che visualizzerà automaticamente un messaggio che indica che è stata rilevata una nuova versione del controllo.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-108">If you have installed the 2.0 version of Microsoft Agent and load a Visual Basic project use the earlier version of the Agent control, Visual Basic includes an option that will automatically display a message indicating that it detected a new version of the control.</span></span> <span data-ttu-id="7f0ad-109">Per assicurare il corretto funzionamento dell'applicazione, scegliere sempre di usare la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-109">To ensure proper operation of your application, always choose to use the later version.</span></span>

<span data-ttu-id="7f0ad-110">Per gli altri linguaggi di programmazione (ad esempio Microsoft Office 97 VBA), per aggiornare il controllo, potrebbe essere necessario rimuovere prima il controllo agente 1,5 e salvare il codice.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-110">For other programming languages (such as Microsoft Office 97 VBA), to update the control, you may have to first remove the 1.5 Agent control and save your code.</span></span> <span data-ttu-id="7f0ad-111">Quindi, chiudere l'ambiente di programmazione, riavviare l'ambiente di programmazione, ricaricare il codice e inserire il nuovo controllo.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-111">Then, quit the programming environment, restart the programming environment, reload your code and insert the new control.</span></span> <span data-ttu-id="7f0ad-112">Evitare di modificare un'applicazione abilitata per Agent 2,0 nella stessa istanza dell'ambiente di programmazione in cui si sta modificando un'applicazione abilitata per Agent 1,5.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-112">Avoid editing an Agent 2.0-enabled application in the same instance of the programming environment that you are editing an Agent 1.5-enabled application in.</span></span> <span data-ttu-id="7f0ad-113">Alcuni ambienti di programmazione potrebbero non gestire le differenze tra le due versioni dei controlli.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-113">Some programming environments may not handle the differences between the two versions of controls.</span></span>

<span data-ttu-id="7f0ad-114">Al termine dell'installazione dell'agente 2,0, dovrebbe essere possibile disinstallare la versione 1,5 dell'agente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-114">You should be able to uninstall the Agent 1.5 release on your system after installing the Agent 2.0 release.</span></span> <span data-ttu-id="7f0ad-115">Tuttavia, se l'agente 1,5 viene installato sulla versione 2,0, potrebbe essere necessario reinstallare 2,0.</span><span class="sxs-lookup"><span data-stu-id="7f0ad-115">However, if Agent 1.5 is installed over the 2.0 release, you may have to reinstall 2.0.</span></span>

 

 




