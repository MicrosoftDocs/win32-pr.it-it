---
description: Windows Installer gli sviluppatori possono creare strumenti che consentono agli utenti finali di usare moduli unione configurabili.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Aggiunta della funzionalità di configurazione del modulo a uno strumento di merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756254"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a><span data-ttu-id="2dd94-103">Aggiunta della funzionalità di configurazione del modulo a uno strumento di merge</span><span class="sxs-lookup"><span data-stu-id="2dd94-103">Adding Module Configuration Capability to a Merge Tool</span></span>

<span data-ttu-id="2dd94-104">Per consentire agli utenti finali di utilizzare i moduli unione configurabili, è possibile creare strumenti di merge e configurazione per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2dd94-104">To enable end users to use configurable merge modules, you can author merge and configuration tools to do the following:</span></span>

-   <span data-ttu-id="2dd94-105">Gli strumenti di merge devono chiamare le funzioni in Mergemod.dll versione 2,0 per unire il modulo.</span><span class="sxs-lookup"><span data-stu-id="2dd94-105">Merge tools should call the functions in Mergemod.dll version 2.0 to merge the module.</span></span> <span data-ttu-id="2dd94-106">Non è possibile usare le versioni precedenti di Mergemod.dll per configurare i moduli unione.</span><span class="sxs-lookup"><span data-stu-id="2dd94-106">Earlier versions of Mergemod.dll cannot be used to configure merge modules.</span></span>
-   <span data-ttu-id="2dd94-107">Le applicazioni di configurazione client devono interagire con l'utente del modulo merge per raccogliere le selezioni utente per gli elementi configurabili.</span><span class="sxs-lookup"><span data-stu-id="2dd94-107">Client configuration applications should interact with the merge module user to collect the user selections for configurable items.</span></span>
-   <span data-ttu-id="2dd94-108">Gli strumenti di merge devono esporre all'applicazione client le informazioni di configurazione create nel modulo merge, in modo che il client possa utilizzare tali informazioni per eseguire query sull'utente.</span><span class="sxs-lookup"><span data-stu-id="2dd94-108">Merge tools should expose configuration information authored into the merge module to the client application so that the client can use this information to query the user.</span></span>
-   <span data-ttu-id="2dd94-109">Quando uno strumento di merge rileva un elemento configurabile durante un'operazione di merge, deve chiamare lo strumento di configurazione client per le informazioni di personalizzazione ottenute dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2dd94-109">When a merge tool encounters a configurable item during a merge, it should call the client configuration tool for customization information obtained from the user.</span></span> <span data-ttu-id="2dd94-110">Lo strumento di merge deve apportare le modifiche specificate al modulo merge.</span><span class="sxs-lookup"><span data-stu-id="2dd94-110">The merge tool should make the specified changes to the merge module.</span></span>
-   <span data-ttu-id="2dd94-111">Le applicazioni di configurazione devono consentire all'utente di fornire scelte per gli elementi configurabili, ma non è necessario che tutte le possibili scelte siano rivelate all'utente.</span><span class="sxs-lookup"><span data-stu-id="2dd94-111">Configuration applications should enable the user to provide choices for configurable items, but all the possible choices do not need to be revealed to the user.</span></span> <span data-ttu-id="2dd94-112">Lo strumento di merge può utilizzare valori predefiniti per gli elementi configurabili non selezionati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2dd94-112">The merge tool can use default values for configurable items that the user does not select.</span></span>
-   <span data-ttu-id="2dd94-113">Se un utente non fornisce informazioni di personalizzazione, gli strumenti di merge devono usare i valori di configurazione predefiniti specificati nel modulo merge.</span><span class="sxs-lookup"><span data-stu-id="2dd94-113">If a user does not provide customization information, merge tools should use the default configuration values that are specified in the merge module.</span></span>
-   <span data-ttu-id="2dd94-114">Dopo che un utente fornisce le selezioni specifiche dello strumento di configurazione, lo strumento di merge chiama Mergemod.dll per eseguire il merge.</span><span class="sxs-lookup"><span data-stu-id="2dd94-114">After a user gives the configuration tool specific selections, the merge tool calls Mergemod.dll to perform the merge.</span></span>

 

 



