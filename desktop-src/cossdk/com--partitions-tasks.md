---
description: Attività partizioni COM+
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: Attività partizioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225585"
---
# <a name="com-partitions-tasks"></a><span data-ttu-id="1c430-103">Attività partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="1c430-103">COM+ Partitions Tasks</span></span>

<span data-ttu-id="1c430-104">Negli argomenti seguenti di questa sezione vengono fornite istruzioni dettagliate per l'utilizzo delle partizioni COM+.</span><span class="sxs-lookup"><span data-stu-id="1c430-104">The following topics in this section provide step-by-step instructions for using COM+ partitions.</span></span>

<span data-ttu-id="1c430-105">**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1c430-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="1c430-106">La partizione globale è l'unica partizione COM+ disponibile.</span><span class="sxs-lookup"><span data-stu-id="1c430-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="1c430-107">\* \* Windows 2000: \* \* il servizio partizioni COM+ non è disponibile in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1c430-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>



| <span data-ttu-id="1c430-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="1c430-108">Topic</span></span>                                                                                                         | <span data-ttu-id="1c430-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c430-109">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c430-110">Creazione e configurazione di partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="1c430-110">Creating and Configuring COM+ Partitions</span></span>](creating-and-configuring-com--partitions.md)<br/>           | <span data-ttu-id="1c430-111">Viene descritto come creare e configurare una partizione COM+.</span><span class="sxs-lookup"><span data-stu-id="1c430-111">Describes how to create and configure a COM+ partition.</span></span><br/>                             |
| [<span data-ttu-id="1c430-112">Gestione delle partizioni locali</span><span class="sxs-lookup"><span data-stu-id="1c430-112">Managing Local Partitions</span></span>](managing-local-partitions.md)<br/>                                         | <span data-ttu-id="1c430-113">Viene descritto come gestire le partizioni COM+ che non si trovano all'interno Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1c430-113">Describes how to manage COM+ partitions that are not within Active Directory.</span></span><br/>       |
| [<span data-ttu-id="1c430-114">Gestione di partizioni all'interno Active Directory</span><span class="sxs-lookup"><span data-stu-id="1c430-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)<br/>     | <span data-ttu-id="1c430-115">Viene descritto come gestire le partizioni COM+ specificate in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1c430-115">Describes how to manage COM+ partitions that are specified within Active Directory.</span></span><br/> |
| [<span data-ttu-id="1c430-116">Impostazione dei diritti amministrativi per una partizione</span><span class="sxs-lookup"><span data-stu-id="1c430-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)<br/> | <span data-ttu-id="1c430-117">Viene descritto come impostare i privilegi di sicurezza per una partizione COM+.</span><span class="sxs-lookup"><span data-stu-id="1c430-117">Describes how to set security privileges for a COM+ partition.</span></span><br/>                      |
| [<span data-ttu-id="1c430-118">Raggruppamento di applicazioni in partizioni</span><span class="sxs-lookup"><span data-stu-id="1c430-118">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)<br/>                 | <span data-ttu-id="1c430-119">Viene descritto come configurare le applicazioni COM+ affinché appartengano a una partizione COM+.</span><span class="sxs-lookup"><span data-stu-id="1c430-119">Describes how to configure COM+ applications to belong to a COM+ partition.</span></span> <br/>        |
| [<span data-ttu-id="1c430-120">Raccolta delle metriche della partizione</span><span class="sxs-lookup"><span data-stu-id="1c430-120">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)<br/>                                   | <span data-ttu-id="1c430-121">Viene descritto come raccogliere dati sulle partizioni COM+.</span><span class="sxs-lookup"><span data-stu-id="1c430-121">Describes how to collect data about COM+ partitions.</span></span><br/>                                |
| [<span data-ttu-id="1c430-122">Configurazione della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="1c430-122">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)<br/>                             | <span data-ttu-id="1c430-123">Viene descritto come configurare la cache della partizione COM+.</span><span class="sxs-lookup"><span data-stu-id="1c430-123">Describes how to configure the COM+ partition cache.</span></span><br/>                                |



 

> [!Note]  
> <span data-ttu-id="1c430-124">Il servizio partizioni COM+ non è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1c430-124">The COM+ Partitions service is not enabled by default.</span></span> <span data-ttu-id="1c430-125">Per utilizzare il servizio partizioni COM+, è necessario abilitarlo tramite lo strumento di amministrazione Servizi componenti o modificando la proprietà PartitionsEnabled nella raccolta [**LocalComputer**](localcomputer.md) su true.</span><span class="sxs-lookup"><span data-stu-id="1c430-125">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1c430-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c430-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c430-127">Concetti relativi alle partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="1c430-127">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)
</dt> </dl>

 

 




