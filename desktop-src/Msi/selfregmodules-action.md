---
description: L'azione SelfRegModules elabora tutti i moduli elencati nella tabella SelfReg e registra tutti i moduli installati con il sistema. Il programma di installazione non registra autonomamente i file EXE.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Azione SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318986"
---
# <a name="selfregmodules-action"></a><span data-ttu-id="f7dcc-104">Azione SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="f7dcc-104">SelfRegModules Action</span></span>

<span data-ttu-id="f7dcc-105">L'azione SelfRegModules elabora tutti i moduli elencati nella tabella [selfreg](selfreg-table.md) e registra tutti i moduli installati con il sistema.</span><span class="sxs-lookup"><span data-stu-id="f7dcc-105">The SelfRegModules action processes all modules listed in the [SelfReg](selfreg-table.md) table and registers all installed modules with the system.</span></span> <span data-ttu-id="f7dcc-106">Il programma di installazione non registra autonomamente i file EXE.</span><span class="sxs-lookup"><span data-stu-id="f7dcc-106">The installer does not self-register EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f7dcc-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="f7dcc-107">Sequence Restrictions</span></span>

<span data-ttu-id="f7dcc-108">Prima di chiamare l'azione SelfRegModules, è necessario chiamare l'azione [InstallValidate](installvalidate-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f7dcc-108">The [InstallValidate](installvalidate-action.md) action must be called before calling the SelfRegModules action.</span></span> <span data-ttu-id="f7dcc-109">Se viene usata un'azione [InstallFiles](installfiles-action.md) , deve essere presente prima dell'azione SelfRegModules nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="f7dcc-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear before the SelfRegModules action in the sequence.</span></span> <span data-ttu-id="f7dcc-110">Poiché l'azione SelfRegModules modifica il sistema, SelfRegModules deve essere seguito dall' [azione InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f7dcc-110">Because the SelfRegModules action changes the system, SelfRegModules should come after the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f7dcc-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="f7dcc-111">ActionData Messages</span></span>



| <span data-ttu-id="f7dcc-112">Campo</span><span class="sxs-lookup"><span data-stu-id="f7dcc-112">Field</span></span> | <span data-ttu-id="f7dcc-113">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="f7dcc-113">Description of action data</span></span>                           |
|-------|------------------------------------------------------|
| <span data-ttu-id="f7dcc-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f7dcc-114">\[1\]</span></span> | <span data-ttu-id="f7dcc-115">Identificatore del file di modulo registrato.</span><span class="sxs-lookup"><span data-stu-id="f7dcc-115">Identifier of registered module file.</span></span>                |
| <span data-ttu-id="f7dcc-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="f7dcc-116">\[2\]</span></span> | <span data-ttu-id="f7dcc-117">Identificatore della cartella che contiene il file del modulo registrato.</span><span class="sxs-lookup"><span data-stu-id="f7dcc-117">Identifier of folder holding registered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f7dcc-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7dcc-118">Remarks</span></span>

<span data-ttu-id="f7dcc-119">L'azione SelfRegModules tenta di chiamare la funzione [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) del modulo pianificato per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="f7dcc-119">The SelfRegModules action attempts to call the [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function of the module scheduled to be registered.</span></span> <span data-ttu-id="f7dcc-120">Questa azione viene eseguita con privilegi elevati quando l'installazione viene eseguita con privilegi elevati, ad esempio durante un'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="f7dcc-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="f7dcc-121">Durante un'installazione per utente, il programma di installazione esegue questa azione con i privilegi utente.</span><span class="sxs-lookup"><span data-stu-id="f7dcc-121">During a per-user installation the installer runs this action with user privileges.</span></span>

<span data-ttu-id="f7dcc-122">Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra la registrazione automatica delle dll usando l' [azione SelfUnRegModules](selfunregmodules-action.md).</span><span class="sxs-lookup"><span data-stu-id="f7dcc-122">Note that you cannot specify the order in which the installer registers self-registering DLLs by using the [SelfUnRegModules action](selfunregmodules-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7dcc-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7dcc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7dcc-124">Specifica dell'ordine di registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="f7dcc-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
