---
description: In alternativa alla gestione delle partizioni Active Directory tramite lo strumento di amministrazione Active Directory utenti e computer, è possibile gestire le partizioni COM+ a livello di codice tramite l'utilizzo di un set di oggetti COM+ all'interno di Active Directory System Interface (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Gestione di partizioni all'interno Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524177"
---
# <a name="managing-partitions-within-active-directory"></a><span data-ttu-id="d48cb-103">Gestione di partizioni all'interno Active Directory</span><span class="sxs-lookup"><span data-stu-id="d48cb-103">Managing Partitions Within Active Directory</span></span>

<span data-ttu-id="d48cb-104">In alternativa alla gestione delle partizioni Active Directory tramite lo strumento di amministrazione Active Directory utenti e computer, è possibile gestire le partizioni COM+ a livello di codice tramite l'utilizzo di un set di oggetti COM+ all'interno di Active Directory System Interface (ADSI).</span><span class="sxs-lookup"><span data-stu-id="d48cb-104">As an alternative to managing Active Directory partitions through the Active Directory Users and Computers administrative tool, you can manage COM+ partitions programmatically through the use of a set of COM+ objects within Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="d48cb-105">Indipendentemente dalla tecnica amministrativa scelta per la gestione delle partizioni COM+, esiste una sequenza generale di passaggi che gli amministratori devono seguire:</span><span class="sxs-lookup"><span data-stu-id="d48cb-105">Regardless of the administrative technique you choose for managing COM+ partitions, there is a general sequence of steps that administrators must follow:</span></span>

1.  <span data-ttu-id="d48cb-106">Creare le nuove partizioni COM+ all'interno Active Directory per il dominio.</span><span class="sxs-lookup"><span data-stu-id="d48cb-106">Create the new COM+ partitions within Active Directory for your domain.</span></span>
2.  <span data-ttu-id="d48cb-107">Creare set di partizioni COM+ all'interno Active Directory ed eseguirne il mapping alle partizioni COM+ appena create.</span><span class="sxs-lookup"><span data-stu-id="d48cb-107">Create COM+ partition sets within Active Directory, and map them to your newly created COM+ partitions.</span></span>
3.  <span data-ttu-id="d48cb-108">Configurare le partizioni Active Directory nel computer locale utilizzando l'oggetto COM+ appropriato.</span><span class="sxs-lookup"><span data-stu-id="d48cb-108">Configure your Active Directory partitions on your local machine, using the appropriate COM+ object.</span></span> <span data-ttu-id="d48cb-109">Quando si configura una partizione Active Directory in un computer locale, nella cartella della partizione viene creata automaticamente una cartella **applicazioni com+** .</span><span class="sxs-lookup"><span data-stu-id="d48cb-109">When you configure an Active Directory partition on a local machine, a **COM+ Applications** folder is automatically created in that partition folder.</span></span>
4.  <span data-ttu-id="d48cb-110">Installare le applicazioni COM+ nelle partizioni COM+ appropriate.</span><span class="sxs-lookup"><span data-stu-id="d48cb-110">Install your COM+ applications in the appropriate COM+ partitions.</span></span>

<span data-ttu-id="d48cb-111">Tutti i passaggi precedenti possono essere eseguiti a livello di codice, usando un set di interfacce di Active Directory denominato ADSI.</span><span class="sxs-lookup"><span data-stu-id="d48cb-111">All of the preceding steps can be done programmatically, using a set of Active Directory interfaces called ADSI.</span></span> <span data-ttu-id="d48cb-112">Gli oggetti disponibili per la gestione delle partizioni disponibili all'interno di ADSI sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d48cb-112">The objects available for managing partitions that are available within ADSI are as follows:</span></span>

-   <span data-ttu-id="d48cb-113">\_nome USERPARTITIONSETLINK \_ DS</span><span class="sxs-lookup"><span data-stu-id="d48cb-113">DS\_USERPARTITIONSETLINK\_NAME</span></span>
-   <span data-ttu-id="d48cb-114">\_nome PARTITIONLINK \_ DS</span><span class="sxs-lookup"><span data-stu-id="d48cb-114">DS\_PARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="d48cb-115">\_nome objectId \_ DS</span><span class="sxs-lookup"><span data-stu-id="d48cb-115">DS\_OBJECTID\_NAME</span></span>
-   <span data-ttu-id="d48cb-116">\_nome DEFAULTPARTITIONLINK \_ DS</span><span class="sxs-lookup"><span data-stu-id="d48cb-116">DS\_DEFAULTPARTITIONLINK\_NAME</span></span>
-   <span data-ttu-id="d48cb-117">\_nome USERLINK \_ DS</span><span class="sxs-lookup"><span data-stu-id="d48cb-117">DS\_USERLINK\_NAME</span></span>
-   <span data-ttu-id="d48cb-118">\_nome partizioni DS \_</span><span class="sxs-lookup"><span data-stu-id="d48cb-118">DS\_PARTITIONSET\_NAME</span></span>
-   <span data-ttu-id="d48cb-119">\_nome partizione \_ DS</span><span class="sxs-lookup"><span data-stu-id="d48cb-119">DS\_PARTITION\_NAME</span></span>

<span data-ttu-id="d48cb-120">Per informazioni sulla creazione e la gestione di partizioni COM+ tramite l'utilizzo degli strumenti di amministrazione Active Directory utenti e computer e Servizi componenti, vedere la guida online disponibile all'interno di ogni strumento.</span><span class="sxs-lookup"><span data-stu-id="d48cb-120">For information on creating and managing COM+ partitions through the use of the Active Directory Users and Computers and Component Services administrative tools, see the online help available from within each tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d48cb-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d48cb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d48cb-122">Raccolta delle metriche della partizione</span><span class="sxs-lookup"><span data-stu-id="d48cb-122">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="d48cb-123">Configurazione della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="d48cb-123">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="d48cb-124">Raggruppamento di applicazioni in partizioni</span><span class="sxs-lookup"><span data-stu-id="d48cb-124">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="d48cb-125">Gestione delle partizioni locali</span><span class="sxs-lookup"><span data-stu-id="d48cb-125">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="d48cb-126">Impostazione dei diritti amministrativi per una partizione</span><span class="sxs-lookup"><span data-stu-id="d48cb-126">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



