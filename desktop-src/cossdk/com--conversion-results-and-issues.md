---
description: Sia che si scelga di convertire i pacchetti MTS in applicazioni COM+ manualmente o che il processo di installazione di Microsoft Windows lo esegua automaticamente, è necessario tenere presenti i risultati della conversione e i problemi.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Risultati e problemi di conversione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401516"
---
# <a name="com-conversion-results-and-issues"></a><span data-ttu-id="0db29-103">Risultati e problemi di conversione COM+</span><span class="sxs-lookup"><span data-stu-id="0db29-103">COM+ Conversion Results and Issues</span></span>

<span data-ttu-id="0db29-104">Sia che si scelga di convertire i pacchetti MTS in applicazioni COM+ manualmente o che il processo di installazione di Microsoft Windows lo esegua automaticamente, è necessario tenere presenti i risultati della conversione e i problemi.</span><span class="sxs-lookup"><span data-stu-id="0db29-104">Whether you choose to convert your MTS packages to COM+ applications manually or let the Microsoft Windows setup process do it for you automatically, you should be aware of the results of conversion as well as the issues.</span></span>

## <a name="what-is-converted"></a><span data-ttu-id="0db29-105">Elementi convertiti</span><span class="sxs-lookup"><span data-stu-id="0db29-105">What Is Converted</span></span>

<span data-ttu-id="0db29-106">Durante la conversione, l'utilità MTSTOCOM converte i ruoli, le assegnazioni di ruolo, le interfacce, i metodi, gli utenti, l'elenco dei computer e la maggior parte delle impostazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="0db29-106">During conversion, the MTSTOCOM utility converts roles, role assignments, interfaces, methods, users, the computer list, and most computer settings.</span></span> <span data-ttu-id="0db29-107">L'utilità MTSTOCOM converte anche l'identità e la password per un pacchetto MTS.</span><span class="sxs-lookup"><span data-stu-id="0db29-107">The MTSTOCOM utility also converts the identity and password for an MTS package.</span></span>

<span data-ttu-id="0db29-108">I nuovi attributi COM+ che non erano disponibili in MTS vengono impostati automaticamente sui valori predefiniti seguenti per tutti i componenti MTS convertiti.</span><span class="sxs-lookup"><span data-stu-id="0db29-108">The new COM+ attributes that were not available in MTS are automatically set to the following defaults for all converted MTS components.</span></span> <span data-ttu-id="0db29-109">Queste impostazioni predefinite possono essere modificate utilizzando lo strumento di amministrazione Servizi componenti o le interfacce amministrative COM+.</span><span class="sxs-lookup"><span data-stu-id="0db29-109">These defaults can be changed using either the Component Services administrative tool or the COM+ administrative interfaces.</span></span>

-   <span data-ttu-id="0db29-110">Attivazione JIT abilitata.</span><span class="sxs-lookup"><span data-stu-id="0db29-110">JIT activation enabled.</span></span>
-   <span data-ttu-id="0db29-111">Pool di oggetti disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0db29-111">Object pooling disabled.</span></span>
-   <span data-ttu-id="0db29-112">Sincronizzazione come impostazione di transazione.</span><span class="sxs-lookup"><span data-stu-id="0db29-112">Synchronization same as Transaction setting.</span></span>

## <a name="conversion-issues"></a><span data-ttu-id="0db29-113">Problemi di conversione</span><span class="sxs-lookup"><span data-stu-id="0db29-113">Conversion Issues</span></span>

<span data-ttu-id="0db29-114">COM+ viene installato automaticamente durante l'installazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="0db29-114">COM+ is automatically installed when you install Windows.</span></span> <span data-ttu-id="0db29-115">Non è possibile disinstallare COM+.</span><span class="sxs-lookup"><span data-stu-id="0db29-115">It is not possible to uninstall COM+.</span></span> <span data-ttu-id="0db29-116">I problemi relativi agli aggiornamenti delle installazioni MTS e COM+ esistenti includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0db29-116">Issues related to upgrades of existing MTS and COM+ installations include the following:</span></span>

-   <span data-ttu-id="0db29-117">Se attualmente si usa MTS 1,0, MTS viene aggiornato automaticamente a COM+.</span><span class="sxs-lookup"><span data-stu-id="0db29-117">If you are currently using MTS 1.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="0db29-118">Tuttavia, i pacchetti definiti dall'utente andranno perduti ed è necessario crearli di nuovo.</span><span class="sxs-lookup"><span data-stu-id="0db29-118">However, user-defined packages will be lost and you must re-create them.</span></span>
-   <span data-ttu-id="0db29-119">Se attualmente si usa MTS 2,0, MTS viene aggiornato automaticamente a COM+.</span><span class="sxs-lookup"><span data-stu-id="0db29-119">If you are currently using MTS 2.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="0db29-120">Tutti i pacchetti definiti dall'utente verranno aggiornati alle applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="0db29-120">All user-defined packages will be upgraded to COM+ applications.</span></span> <span data-ttu-id="0db29-121">Tutti i componenti dovrebbero funzionare come in MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="0db29-121">All components should work as they did under MTS 2.0.</span></span>
-   <span data-ttu-id="0db29-122">Se si usano MTS 1,0 e MTS 2,0 e si è installata l'opzione SDK, i file dell'SDK verranno rimossi.</span><span class="sxs-lookup"><span data-stu-id="0db29-122">If you are using MTS 1.0 and MTS 2.0 and have installed the SDK option, the SDK files will be removed.</span></span> <span data-ttu-id="0db29-123">È possibile installare la versione più recente di COM+ SDK tramite il Microsoft Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0db29-123">You can install the latest COM+ SDK through the Microsoft Windows SDK.</span></span>
-   <span data-ttu-id="0db29-124">Non è possibile gestire un computer MTS remoto da un computer COM+.</span><span class="sxs-lookup"><span data-stu-id="0db29-124">You cannot manage a remote MTS computer from a COM+ computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0db29-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0db29-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0db29-126">Conversione automatica da MTS</span><span class="sxs-lookup"><span data-stu-id="0db29-126">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="0db29-127">Conversione manuale da MTS</span><span class="sxs-lookup"><span data-stu-id="0db29-127">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="0db29-128">Libreria di amministrazione MTS</span><span class="sxs-lookup"><span data-stu-id="0db29-128">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



