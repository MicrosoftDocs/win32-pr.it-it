---
title: IRootStorage-implementazione del file composto
description: L'implementazione del file composto di COM di IRootStorage consente di salvare i file in situazioni di memoria insufficiente o di spazio su disco insufficiente. Per informazioni sul comportamento di questa interfaccia, vedere IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714569"
---
# <a name="irootstorage---compound-file-implementation"></a><span data-ttu-id="cea30-105">IRootStorage-implementazione del file composto</span><span class="sxs-lookup"><span data-stu-id="cea30-105">IRootStorage - Compound File Implementation</span></span>

<span data-ttu-id="cea30-106">L'implementazione del file composto di COM di [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) consente di salvare i file in situazioni di memoria insufficiente o di spazio su disco insufficiente.</span><span class="sxs-lookup"><span data-stu-id="cea30-106">COM's compound file implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) allows you to support saving files in low-memory or low disk-space situations.</span></span> <span data-ttu-id="cea30-107">Per informazioni sul comportamento di questa interfaccia, vedere **IRootStorage**.</span><span class="sxs-lookup"><span data-stu-id="cea30-107">For information on how this interface behaves, see **IRootStorage**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cea30-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="cea30-108">When to Use</span></span>

<span data-ttu-id="cea30-109">Usare l'implementazione fornita dal sistema di [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) solo per supportare il salvataggio di file in condizioni di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="cea30-109">Use the system-supplied implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) only to support saving files under low-memory conditions.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea30-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cea30-110">Remarks</span></span>

<span data-ttu-id="cea30-111">È possibile chiamare l'implementazione di COM di [**IRootStorage:: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) per eseguire una normale operazione di salvataggio in un altro file.</span><span class="sxs-lookup"><span data-stu-id="cea30-111">It is possible to call COM's implementation of [**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) to do a normal save-as operation to another file.</span></span> <span data-ttu-id="cea30-112">Tuttavia, le applicazioni che eseguono questa operazione potrebbero non essere compatibili con le generazioni future di archiviazione COM.</span><span class="sxs-lookup"><span data-stu-id="cea30-112">However, applications that do this might not be compatible with future generations of COM storage.</span></span> <span data-ttu-id="cea30-113">Per evitare questa possibilità, le applicazioni che eseguono un'operazione di salvataggio devono creare manualmente il secondo file composto e richiamare [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span><span class="sxs-lookup"><span data-stu-id="cea30-113">To avoid this possibility, applications performing a save-as operation should manually create the second compound file and invoke [**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span></span> <span data-ttu-id="cea30-114">Il metodo **IRootStorage:: SwitchToFile** deve essere usato solo in situazioni di emergenza (memoria insufficiente o spazio su disco).</span><span class="sxs-lookup"><span data-stu-id="cea30-114">The **IRootStorage::SwitchToFile** method should be used only in emergency (low-memory or disk-space) situations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cea30-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cea30-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cea30-116">**IRootStorage**</span><span class="sxs-lookup"><span data-stu-id="cea30-116">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="cea30-117">**IRootStorage::SwitchToFile**</span><span class="sxs-lookup"><span data-stu-id="cea30-117">**IRootStorage::SwitchToFile**</span></span>](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




