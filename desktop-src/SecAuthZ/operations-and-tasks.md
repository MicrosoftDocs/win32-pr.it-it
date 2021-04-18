---
description: Un'operazione è un'azione del computer di basso livello.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Operazioni e attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314728"
---
# <a name="operations-and-tasks"></a><span data-ttu-id="e9d03-103">Operazioni e attività</span><span class="sxs-lookup"><span data-stu-id="e9d03-103">Operations and Tasks</span></span>

<span data-ttu-id="e9d03-104">Un'operazione è un'azione del computer di basso livello.</span><span class="sxs-lookup"><span data-stu-id="e9d03-104">An operation is a low-level computer action.</span></span> <span data-ttu-id="e9d03-105">Nell'API di gestione autorizzazioni un'operazione è rappresentata da un oggetto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="e9d03-105">In the Authorization Manager API, an operation is represented by an [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) object.</span></span> <span data-ttu-id="e9d03-106">In generale, le operazioni sono troppo numerose e di basso livello per facilitare l'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="e9d03-106">In general, operations are too many in number and too low-level to facilitate administration.</span></span> <span data-ttu-id="e9d03-107">Raggruppare le operazioni nelle attività per semplificare l'amministrazione dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="e9d03-107">Group operations into tasks to simplify administration of authorization policy.</span></span>

<span data-ttu-id="e9d03-108">Un'attività è rappresentata da un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) e può contenere uno o più oggetti [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="e9d03-108">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object and can contain one or more [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) objects.</span></span> <span data-ttu-id="e9d03-109">Un oggetto **IAzTask** può inoltre contenere altri oggetti **IAzTask** , in modo che le attività possano essere annidate.</span><span class="sxs-lookup"><span data-stu-id="e9d03-109">An **IAzTask** object can also contain other **IAzTask** objects, so that tasks can be nested.</span></span> <span data-ttu-id="e9d03-110">Per semplificare l'amministrazione, un oggetto **IAzTask** deve rappresentare un'attività che un utente reale vuole eseguire.</span><span class="sxs-lookup"><span data-stu-id="e9d03-110">To facilitate administration, an **IAzTask** object should represent a task that a real user wants to perform.</span></span>

<span data-ttu-id="e9d03-111">L'accesso alle operazioni contenute in un'attività può essere qualificato in fase di esecuzione da uno script della regola di business associato all'oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) che rappresenta tale attività.</span><span class="sxs-lookup"><span data-stu-id="e9d03-111">Access to the operations contained by a task can be qualified at run time by a business rule script associated with the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents that task.</span></span> <span data-ttu-id="e9d03-112">Per ulteriori informazioni sugli script delle regole business, vedere [regole business](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="e9d03-112">For more information about business rule scripts, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="e9d03-113">Un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) può anche rappresentare una definizione di ruolo impostando la relativa proprietà [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) su **true**.</span><span class="sxs-lookup"><span data-stu-id="e9d03-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can also represent a role definition by setting its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property to **TRUE**.</span></span> <span data-ttu-id="e9d03-114">L'interfaccia utente dello snap-in MMC di **Gestione autorizzazioni** Visualizza quindi l'oggetto **IAzTask** come ruolo.</span><span class="sxs-lookup"><span data-stu-id="e9d03-114">The **Authorization Manager** MMC snap-in user interface then displays that **IAzTask** object as a role.</span></span> <span data-ttu-id="e9d03-115">Per ulteriori informazioni sulle definizioni di ruolo, vedere [ruoli](roles.md).</span><span class="sxs-lookup"><span data-stu-id="e9d03-115">For more information about role definitions, see [Roles](roles.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9d03-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9d03-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9d03-117">Definizione di operazioni in C++</span><span class="sxs-lookup"><span data-stu-id="e9d03-117">Defining Operations in C++</span></span>](defining-operations-in-c--.md)
</dt> <dt>

[<span data-ttu-id="e9d03-118">Raggruppamento di operazioni in attività in C++</span><span class="sxs-lookup"><span data-stu-id="e9d03-118">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[<span data-ttu-id="e9d03-119">Raggruppamento di attività in ruoli in C++</span><span class="sxs-lookup"><span data-stu-id="e9d03-119">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="e9d03-120">Utenti e gruppi</span><span class="sxs-lookup"><span data-stu-id="e9d03-120">Users and Groups</span></span>](users-and-groups.md)
</dt> </dl>

 

 



