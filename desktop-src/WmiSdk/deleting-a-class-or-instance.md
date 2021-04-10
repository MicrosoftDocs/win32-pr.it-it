---
description: Al termine di una classe o di un'istanza di, è possibile eliminare la classe o l'istanza da WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Eliminazione di una classe o di un'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226950"
---
# <a name="deleting-a-class-or-instance"></a><span data-ttu-id="8548d-103">Eliminazione di una classe o di un'istanza</span><span class="sxs-lookup"><span data-stu-id="8548d-103">Deleting a Class or Instance</span></span>

<span data-ttu-id="8548d-104">Al termine di una classe o di un'istanza di, è possibile eliminare la classe o l'istanza da WMI.</span><span class="sxs-lookup"><span data-stu-id="8548d-104">After you finish with a class or an instance, you may wish to delete that class or instance from WMI.</span></span> <span data-ttu-id="8548d-105">Analogamente ad altre tecnologie orientate agli oggetti, è possibile eliminare oggetti di classe o istanza per pulire lo spazio dei nomi WMI e restituire le risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="8548d-105">Like other object-oriented technologies, you can delete class or instance objects to clean up the WMI namespace and to return system resources.</span></span> <span data-ttu-id="8548d-106">Tuttavia, molte classi e istanze in WMI sono persistenti e vengono usate da un'ampia gamma di applicazioni in qualsiasi momento, pertanto è necessario prestare attenzione quando si elimina una classe o un'istanza WMI: l'applicazione o un'altra applicazione richiederà probabilmente la classe o l'istanza in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="8548d-106">However, many classes and instances in WMI are persistent and are used by a variety of applications at any given time Therefore, you should be careful when deleting a WMI class or instance: your application or another application will probably need the class or instance at a later date.</span></span>

<span data-ttu-id="8548d-107">L'eliminazione di una classe o di un'istanza è una procedura semplice.</span><span class="sxs-lookup"><span data-stu-id="8548d-107">Deleting a class or an instance is a simple procedure.</span></span> <span data-ttu-id="8548d-108">Tuttavia, a causa della natura permanente di una classe, probabilmente non sarà necessario eliminare spesso una classe.</span><span class="sxs-lookup"><span data-stu-id="8548d-108">However, due to the permanent nature of a class, you will probably not need to delete a class often.</span></span> <span data-ttu-id="8548d-109">È possibile, ad esempio, eliminare la classe [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , perché è improbabile che non si disponga di un'unità disco in un punto qualsiasi dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="8548d-109">For example, you are unlikely to delete the [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) class, because it is unlikely that you do not have a disk drive somewhere in your enterprise.</span></span> <span data-ttu-id="8548d-110">In alternativa, sarà più probabile eliminare un'istanza di una classe.</span><span class="sxs-lookup"><span data-stu-id="8548d-110">Instead, you will be more likely to delete an instance of a class.</span></span> <span data-ttu-id="8548d-111">Per ulteriori informazioni, vedere [eliminazione di un'istanza](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="8548d-111">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span>

<span data-ttu-id="8548d-112">Sebbene non comune, è possibile che si verifichi un periodo di tempo in cui si desidera aggiornare una classe creata.</span><span class="sxs-lookup"><span data-stu-id="8548d-112">Although uncommon, you may come across a time where you wish to update a class that you created.</span></span> <span data-ttu-id="8548d-113">Ad esempio, è possibile creare una classe per rappresentare un'applicazione di terze parti.</span><span class="sxs-lookup"><span data-stu-id="8548d-113">For example, you could create a class to represent a third-party application.</span></span> <span data-ttu-id="8548d-114">Se il software di terze parti è stato aggiornato nella misura in cui la classe non rappresenta più correttamente il software, potrebbe essere necessario eliminare la classe originale.</span><span class="sxs-lookup"><span data-stu-id="8548d-114">If the third-party updated their software to the extent that your class no longer properly represented the software, you may need to delete your original class.</span></span> <span data-ttu-id="8548d-115">Per ulteriori informazioni, vedere [eliminazione di una classe](deleting-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="8548d-115">For more information, see [Deleting a Class](deleting-a-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8548d-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8548d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8548d-117">Progettazione di classi Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="8548d-117">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
