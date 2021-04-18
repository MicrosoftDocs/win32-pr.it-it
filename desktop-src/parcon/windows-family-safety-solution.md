---
description: Soluzione di sicurezza della famiglia di Windows
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Soluzione di sicurezza della famiglia di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318392"
---
# <a name="windows-family-safety-solution"></a><span data-ttu-id="13ec6-103">Soluzione di sicurezza della famiglia di Windows</span><span class="sxs-lookup"><span data-stu-id="13ec6-103">Windows Family Safety Solution</span></span>

<span data-ttu-id="13ec6-104">Di seguito sono riportati i requisiti chiave definiti da Microsoft per una soluzione più completa.</span><span class="sxs-lookup"><span data-stu-id="13ec6-104">Key requirements defined by Microsoft for a more comprehensive solution are as follows.</span></span> <span data-ttu-id="13ec6-105">Si noti che la definizione di online è una tecnologia principalmente connessa a Internet, a differenza di un client offline che in genere è limitato al computer.</span><span class="sxs-lookup"><span data-stu-id="13ec6-105">Note the definition for online is a primarily Internet-facing technology, unlike an offline client which is usually bounded at the computer.</span></span>

-   <span data-ttu-id="13ec6-106">Fornire un'unica area facile da trovare nell'interfaccia utente del sistema operativo in cui tutti i criteri dei controlli padre, il controllo del monitoraggio delle attività e i dati delle attività per un'identità possono essere individuati facilmente.</span><span class="sxs-lookup"><span data-stu-id="13ec6-106">Provide a single, easy to find area in the operating system user interface where all parental controls policies, control of activity monitoring, and activity data for an identity may be readily discovered.</span></span>

-   <span data-ttu-id="13ec6-107">Supportare il monitoraggio di attività sufficienti dell'utente controllato in modo che un genitore o un tutore abbia una ragionevole confidenza per individuare le attività rischiose.</span><span class="sxs-lookup"><span data-stu-id="13ec6-107">Support monitoring of sufficient activity of the controlled user so that a parent or guardian has reasonable confidence that risky activities may be discovered.</span></span> <span data-ttu-id="13ec6-108">Inoltre, riconfigurare il log dei criteri dell'utente controllato in modo che le modifiche non intenzionali o non autorizzate siano individuabili.</span><span class="sxs-lookup"><span data-stu-id="13ec6-108">Also, log reconfiguration of the controlled user's policies so that unintended or unauthorized changes are discoverable.</span></span>

-   <span data-ttu-id="13ec6-109">Esporre le funzionalità di monitoraggio delle attività tramite le interfacce di registrazione eventi standard di Windows Vista e fornire una soluzione di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="13ec6-109">Expose activity monitoring capabilities through standard Windows Vista event logging interfaces, and provide an in-box viewer solution.</span></span> <span data-ttu-id="13ec6-110">Definire gli eventi di attività standard e garantire l'estendibilità per la generazione di eventi personalizzati da parte degli ISV.</span><span class="sxs-lookup"><span data-stu-id="13ec6-110">Define standard activity events, and provide for extensibility to custom event generation by ISVs.</span></span>

-   <span data-ttu-id="13ec6-111">Promuovere che tutti i monitoraggi e le restrizioni per un utente siano attivati solo in base ai genitori o ai tutori.</span><span class="sxs-lookup"><span data-stu-id="13ec6-111">Promote that all monitoring and restrictions for a user are turned on only on an opt-in basis by parents or guardians.</span></span> <span data-ttu-id="13ec6-112">Laddove possibile, la funzionalità delle restrizioni deve essere completamente inattiva per gli utenti non controllati per ridurre al minimo i rischi per la sicurezza e la compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="13ec6-112">Wherever possible, restrictions functionality should be completely inactive for non-controlled users to minimize security and application compatibility risks.</span></span>

-   <span data-ttu-id="13ec6-113">Microsoft si impegnerà, laddove possibile, a non prendere decisioni di valore in base all'età o ad altri parametri per l'utente controllato (le terze parti possono scegliere di farlo).</span><span class="sxs-lookup"><span data-stu-id="13ec6-113">Microsoft shall strive, whenever possible, not to make value judgments by age or other parameters for the controlled user (third parties may choose to do so).</span></span> <span data-ttu-id="13ec6-114">Tali decisioni vengono rilasciate al padre o al tutore, spesso influenzato da community o organizzazioni.</span><span class="sxs-lookup"><span data-stu-id="13ec6-114">Such decisions are left up to the parent or guardian, often influenced by communities or organizations.</span></span>

-   <span data-ttu-id="13ec6-115">Fornire le implementazioni nel prodotto per il monitoraggio e le restrizioni delle attività offline, in cui sono attualmente disponibili alcune o nessuna offerta, in cui la funzionalità associata al rischio di sicurezza è disponibile nel prodotto o quando una soluzione Microsoft fornisce funzionalità efficaci e affidabili completamente integrate con la progettazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="13ec6-115">Provide implementations in the product for offline activity monitoring and restrictions where few or no offerings are available today, where the associated safety-risk functionality is available in the product, or where a Microsoft solution provides capable and robust functionality fully integrated with the design of the operating system.</span></span>

-   <span data-ttu-id="13ec6-116">In generale, alzare di livello le applicazioni per eseguire la registrazione e le restrizioni per ottimizzare il contesto e l'esperienza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="13ec6-116">Generally, promote that applications perform their own logging and restrictions for best context and UI experience.</span></span>

    <span data-ttu-id="13ec6-117">Eccezione: fornire funzionalità complete di monitoraggio e restrizione delle attività in linea nelle aree selezionate in cui i vantaggi per i consumer e il settore superano i costi.</span><span class="sxs-lookup"><span data-stu-id="13ec6-117">Exception: Provide comprehensive online activity monitoring and restrictions in selected areas where the benefit to consumers and industry outweigh the costs.</span></span>

-   <span data-ttu-id="13ec6-118">Esporre i controlli padre le impostazioni dell'interfaccia utente e le definizioni degli eventi di attività usando le API pubbliche in modo che le terze parti possano eseguire query per lo stato, modificare le impostazioni e leggere i log attività se sono in esecuzione con privilegi di account di Windows sufficienti.</span><span class="sxs-lookup"><span data-stu-id="13ec6-118">Expose parental controls user interface settings and activity event definitions by using public APIs so that third parties may query for state, modify settings, and read activity logs if they are running with sufficient Windows account privileges.</span></span>

<span data-ttu-id="13ec6-119">Un obiettivo fondamentale è promuovere la coesistenza delle soluzioni di controllo parentale di terze parti con la funzionalità integrata e supportare l'aggiunta di valore tramite l'integrazione di, l'estensione o la fornitura di funzionalità alternative laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="13ec6-119">An overarching goal is to promote third-party parental controls solutions' coexistence with the in-box functionality, and support adding value by integrating with, extending, or providing alternative capabilities where suitable.</span></span>

 

 



