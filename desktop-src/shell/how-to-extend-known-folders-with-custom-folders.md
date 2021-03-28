---
description: I fornitori di software indipendenti (ISV) possono estendere il set di cartelle note in un sistema registrando le cartelle note.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Come estendere le cartelle note con cartelle personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227436"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a><span data-ttu-id="99180-103">Come estendere le cartelle note con cartelle personalizzate</span><span class="sxs-lookup"><span data-stu-id="99180-103">How to Extend Known Folders with Custom Folders</span></span>

<span data-ttu-id="99180-104">I fornitori di software indipendenti (ISV) possono estendere il set di cartelle note in un sistema registrando le cartelle note.</span><span class="sxs-lookup"><span data-stu-id="99180-104">Independent software vendors (ISVs) can extend the set of known folders on a system by registering known folders of their own.</span></span> <span data-ttu-id="99180-105">Una volta registrate, le cartelle di terze parti sono note al sistema.</span><span class="sxs-lookup"><span data-stu-id="99180-105">Once registered, those third-party folders are known to the system.</span></span> <span data-ttu-id="99180-106">Vengono rilevate da qualsiasi chiamata a [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span><span class="sxs-lookup"><span data-stu-id="99180-106">They are found by any call to [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span></span> <span data-ttu-id="99180-107">Si noti che una cartella nota deve essere una cartella per computer.</span><span class="sxs-lookup"><span data-stu-id="99180-107">Note that a known folder must be a per-machine folder.</span></span> <span data-ttu-id="99180-108">Non è possibile creare una cartella nota per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="99180-108">You cannot create a per-user known folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="99180-109">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="99180-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="99180-110">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="99180-110">Step 1:</span></span>

<span data-ttu-id="99180-111">Definire la cartella nota tramite una struttura di [**\_ definizione cartellanota**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .</span><span class="sxs-lookup"><span data-stu-id="99180-111">Define your known folder through a [**KNOWNFOLDER\_DEFINITION**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) structure.</span></span>

### <a name="step-2"></a><span data-ttu-id="99180-112">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="99180-112">Step 2:</span></span>

<span data-ttu-id="99180-113">Registrare la cartella nota tramite una chiamata a [**IKnownFolderManager:: RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span><span class="sxs-lookup"><span data-stu-id="99180-113">Register the known folder through a call to [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span></span>

## <a name="remarks"></a><span data-ttu-id="99180-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="99180-114">Remarks</span></span>

<span data-ttu-id="99180-115">Se si crea una cartella nota per l'applicazione come parte della procedura di installazione, è necessario includere anche [**IKnownFolderManager:: UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) come parte del codice di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="99180-115">If you create a known folder for your application as part of your installation procedure, you must also include [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) as part of your uninstallation code.</span></span>

<span data-ttu-id="99180-116">Tenere in considerazione i motivi per cui si desidera che la cartella venga inclusa nel sistema di cartelle note prima di registrarla.</span><span class="sxs-lookup"><span data-stu-id="99180-116">Give consideration to why you want your folder to be included in the known folder system before you register it.</span></span> <span data-ttu-id="99180-117">È necessario avere un motivo valido per elevare la cartella a tale livello di visibilità del sistema.</span><span class="sxs-lookup"><span data-stu-id="99180-117">You should have a valid reason for elevating your folder to that level of system visibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99180-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99180-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="99180-119">[Esempio di cartelle note](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99180-119">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
