---
title: Interfacce QMGR
description: Utilizzare le seguenti interfacce di gestione code (QMGR) per scaricare i file e monitorare i processi nella coda di download.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220972"
---
# <a name="qmgr-interfaces"></a><span data-ttu-id="8b174-103">Interfacce QMGR</span><span class="sxs-lookup"><span data-stu-id="8b174-103">QMGR Interfaces</span></span>

<span data-ttu-id="8b174-104">\[Le interfacce di gestione code (QMGR) sono disponibili per l'uso nei sistemi operativi specificati nella sezione requisiti di un argomento.</span><span class="sxs-lookup"><span data-stu-id="8b174-104">\[Queue Manager (QMGR) interfaces are available for use in the operating systems specified in a topic's Requirements section.</span></span> <span data-ttu-id="8b174-105">Possono essere modificati o non disponibili nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8b174-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8b174-106">Usare invece le [interfacce bits](bits-interfaces.md).\]</span><span class="sxs-lookup"><span data-stu-id="8b174-106">Instead, use the [BITS interfaces](bits-interfaces.md).\]</span></span>

<span data-ttu-id="8b174-107">Utilizzare le seguenti interfacce di gestione code (QMGR) per scaricare i file e monitorare i processi nella coda di download.</span><span class="sxs-lookup"><span data-stu-id="8b174-107">Use the following Queue Manager (QMGR) interfaces to download files and monitor jobs within the download queue.</span></span>



| <span data-ttu-id="8b174-108">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="8b174-108">Interface</span></span>                                                                 | <span data-ttu-id="8b174-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b174-109">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b174-110">**IBackgroundCopyCallback1**</span><span class="sxs-lookup"><span data-stu-id="8b174-110">**IBackgroundCopyCallback1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | <span data-ttu-id="8b174-111">Implementare per ricevere una notifica quando si verificano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="8b174-111">Implement to receive notification when events occur.</span></span><br/>                                                                                               |
| [<span data-ttu-id="8b174-112">**IBackgroundCopyGroup**</span><span class="sxs-lookup"><span data-stu-id="8b174-112">**IBackgroundCopyGroup**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | <span data-ttu-id="8b174-113">Utilizzare per gestire il gruppo.</span><span class="sxs-lookup"><span data-stu-id="8b174-113">Use to manage the group.</span></span> <span data-ttu-id="8b174-114">Ad esempio, aggiungere un processo al gruppo, impostare le proprietà del gruppo e avviare e arrestare il gruppo nella coda di download.</span><span class="sxs-lookup"><span data-stu-id="8b174-114">For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.</span></span><br/> |
| [<span data-ttu-id="8b174-115">**IBackgroundCopyJob1**</span><span class="sxs-lookup"><span data-stu-id="8b174-115">**IBackgroundCopyJob1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | <span data-ttu-id="8b174-116">Usare per aggiungere file al processo e recuperare lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="8b174-116">Use to add files to the job and retrieve the job's status.</span></span><br/>                                                                                         |
| [<span data-ttu-id="8b174-117">**IBackgroundCopyQMgr**</span><span class="sxs-lookup"><span data-stu-id="8b174-117">**IBackgroundCopyQMgr**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | <span data-ttu-id="8b174-118">Utilizzare per creare un nuovo gruppo, recuperare un gruppo esistente o enumerare tutti i gruppi nella coda.</span><span class="sxs-lookup"><span data-stu-id="8b174-118">Use to create a new group, retrieve an existing group, or enumerate all groups in the queue.</span></span><br/>                                                       |
| [<span data-ttu-id="8b174-119">**IEnumBackgroundCopyGroups**</span><span class="sxs-lookup"><span data-stu-id="8b174-119">**IEnumBackgroundCopyGroups**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | <span data-ttu-id="8b174-120">Utilizzare per recuperare un elenco di gruppi nella coda di download.</span><span class="sxs-lookup"><span data-stu-id="8b174-120">Use to retrieve a list of groups in the download queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="8b174-121">**IEnumBackgroundCopyJobs1**</span><span class="sxs-lookup"><span data-stu-id="8b174-121">**IEnumBackgroundCopyJobs1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | <span data-ttu-id="8b174-122">Utilizzare per recuperare un elenco di processi nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="8b174-122">Use to retrieve a list of jobs in the group.</span></span><br/>                                                                                                       |



 

 

 





