---
description: L'azione SelfUnregModules Annulla la registrazione di tutti i moduli elencati nella tabella SelfReg che sono pianificati per la disinstallazione. Il programma di installazione non esegue la registrazione automatica. File EXE.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Azione SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318987"
---
# <a name="selfunregmodules-action"></a><span data-ttu-id="ff257-104">Azione SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="ff257-104">SelfUnregModules Action</span></span>

<span data-ttu-id="ff257-105">L'azione SelfUnregModules Annulla la registrazione di tutti i moduli elencati nella [tabella SelfReg](selfreg-table.md) che sono pianificati per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="ff257-105">The SelfUnregModules action unregisters all modules listed in the [SelfReg table](selfreg-table.md) that are scheduled to be uninstalled.</span></span> <span data-ttu-id="ff257-106">Il programma di installazione non esegue la registrazione automatica. File EXE.</span><span class="sxs-lookup"><span data-stu-id="ff257-106">The installer does not self-register .EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ff257-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="ff257-107">Sequence Restrictions</span></span>

<span data-ttu-id="ff257-108">L'azione [InstallValidate](installvalidate-action.md) deve essere presente prima dell'azione SelfUnregModules nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="ff257-108">The [InstallValidate](installvalidate-action.md) action must appear before the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="ff257-109">Se viene utilizzata un'azione [SelfRegModules](selfregmodules-action.md) , deve comparire dopo l'azione SelfUnregModules nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="ff257-109">If a [SelfRegModules](selfregmodules-action.md) action is used it must appear after the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="ff257-110">Se viene utilizzata un' [azione RemoveFiles](removefiles-action.md) , deve comparire dopo l'azione SelfUnregModules nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="ff257-110">If a [RemoveFiles action](removefiles-action.md) is used it must appear after the SelfUnregModules action in the sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ff257-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="ff257-111">ActionData Messages</span></span>



| <span data-ttu-id="ff257-112">Campo</span><span class="sxs-lookup"><span data-stu-id="ff257-112">Field</span></span> | <span data-ttu-id="ff257-113">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="ff257-113">Description of action data</span></span>                             |
|-------|--------------------------------------------------------|
| <span data-ttu-id="ff257-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ff257-114">\[1\]</span></span> | <span data-ttu-id="ff257-115">Identificatore del file di modulo non registrato.</span><span class="sxs-lookup"><span data-stu-id="ff257-115">Identifier of unregistered module file.</span></span>                |
| <span data-ttu-id="ff257-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ff257-116">\[2\]</span></span> | <span data-ttu-id="ff257-117">Identificatore della cartella che contiene il file del modulo non registrato.</span><span class="sxs-lookup"><span data-stu-id="ff257-117">Identifier of folder holding unregistered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ff257-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff257-118">Remarks</span></span>

<span data-ttu-id="ff257-119">L'azione SelfUnregModules tenta di chiamare la funzione [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) del modulo di cui deve essere annullata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="ff257-119">The SelfUnregModules action attempts to call the [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) function of the module that is to be unregistered.</span></span> <span data-ttu-id="ff257-120">Questa azione viene eseguita con privilegi elevati quando l'installazione viene eseguita con privilegi elevati, ad esempio durante un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="ff257-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="ff257-121">Durante un'installazione per utente, il programma di installazione esegue questa azione con i privilegi utente.</span><span class="sxs-lookup"><span data-stu-id="ff257-121">During a per-user installation, the installer runs this action with user privileges.</span></span>

<span data-ttu-id="ff257-122">Si noti che non è possibile specificare l'ordine in cui il programma di installazione Annulla la registrazione automatica delle dll usando l'azione SelfUnRegModules.</span><span class="sxs-lookup"><span data-stu-id="ff257-122">Note that you cannot specify the order in which the installer unregisters self-registering DLLs by using the SelfUnRegModules action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff257-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff257-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff257-124">Specifica dell'ordine di registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="ff257-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
