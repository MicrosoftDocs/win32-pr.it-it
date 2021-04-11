---
description: Istruzioni per l'utilizzo dell'API di gestione autorizzazioni per creare un archivio criteri di autorizzazione nello script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Creazione di un archivio criteri di autorizzazione nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130655"
---
# <a name="creating-an-authorization-policy-store-in-script"></a><span data-ttu-id="b9da6-103">Creazione di un archivio criteri di autorizzazione nello script</span><span class="sxs-lookup"><span data-stu-id="b9da6-103">Creating an Authorization Policy Store in Script</span></span>

<span data-ttu-id="b9da6-104">Creare un criterio di autorizzazione prima o durante l'installazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9da6-104">Create an authorization policy before or during the installation of an application.</span></span>

<span data-ttu-id="b9da6-105">Quando si usa l'API di gestione autorizzazioni per creare un criterio di autorizzazione, seguire le istruzioni fornite negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b9da6-105">When you use the Authorization Manager API to create an authorization policy, follow the instructions provided in the following topics.</span></span>



| <span data-ttu-id="b9da6-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="b9da6-106">Topic</span></span>                                                                                                                  | <span data-ttu-id="b9da6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9da6-107">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9da6-108">Creazione di un oggetto archivio criteri di autorizzazione nello script</span><span class="sxs-lookup"><span data-stu-id="b9da6-108">Creating an Authorization Policy Store Object in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md) | <span data-ttu-id="b9da6-109">Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di sicurezza di un'applicazione o di un gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b9da6-109">An authorization policy store contains information about the security policy of an application or group of applications.</span></span>                                                                                                                                       |
| [<span data-ttu-id="b9da6-110">Creazione di un oggetto applicazione nello script</span><span class="sxs-lookup"><span data-stu-id="b9da6-110">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)                               | <span data-ttu-id="b9da6-111">Per ogni applicazione che usa un archivio criteri di autorizzazione, è necessario creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvarlo in un archivio criteri.</span><span class="sxs-lookup"><span data-stu-id="b9da6-111">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>                                                                                                |
| [<span data-ttu-id="b9da6-112">Definizione di operazioni nello script</span><span class="sxs-lookup"><span data-stu-id="b9da6-112">Defining Operations in Script</span></span>](defining-operations-in-script.md)                                                     | <span data-ttu-id="b9da6-113">Un'operazione è una funzione o un metodo di basso livello di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9da6-113">An operation is a low-level function or method of an application.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="b9da6-114">Raggruppamento di operazioni in attività nello script</span><span class="sxs-lookup"><span data-stu-id="b9da6-114">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)                               | <span data-ttu-id="b9da6-115">Un'attività è un'azione di alto livello che gli utenti di un'applicazione devono completare.</span><span class="sxs-lookup"><span data-stu-id="b9da6-115">A task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="b9da6-116">Le attività sono costituite da operazioni, ovvero funzioni di basso livello e metodi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9da6-116">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span>                                                                                    |
| [<span data-ttu-id="b9da6-117">Raggruppamento di attività in ruoli nello script</span><span class="sxs-lookup"><span data-stu-id="b9da6-117">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)                                         | <span data-ttu-id="b9da6-118">Un ruolo rappresenta una categoria di utenti e le attività che gli utenti sono autorizzati a eseguire.</span><span class="sxs-lookup"><span data-stu-id="b9da6-118">A role represents a category of users and the tasks those users are authorized to perform.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="b9da6-119">Definizione di gruppi di utenti nello script</span><span class="sxs-lookup"><span data-stu-id="b9da6-119">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)                                           | <span data-ttu-id="b9da6-120">Un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) rappresenta un gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="b9da6-120">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="b9da6-121">I ruoli possono quindi essere assegnati a questo gruppo di utenti collettivamente.</span><span class="sxs-lookup"><span data-stu-id="b9da6-121">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="b9da6-122">Un oggetto **IAzApplicationGroup** può includere anche altri oggetti **IAzApplicationGroup** come membri.</span><span class="sxs-lookup"><span data-stu-id="b9da6-122">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> |
| [<span data-ttu-id="b9da6-123">Aggiunta di utenti a un gruppo di applicazioni nello script</span><span class="sxs-lookup"><span data-stu-id="b9da6-123">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)                   | <span data-ttu-id="b9da6-124">Un gruppo di applicazioni è un gruppo di utenti e gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="b9da6-124">An application group is a group of users and user groups.</span></span> <span data-ttu-id="b9da6-125">Un gruppo di applicazioni può contenere altri gruppi di applicazioni, quindi i gruppi di utenti possono essere annidati.</span><span class="sxs-lookup"><span data-stu-id="b9da6-125">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="b9da6-126">Un gruppo di applicazioni è rappresentato da un oggetto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="b9da6-126">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>    |



 

 

 



