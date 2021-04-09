---
description: Interfacce del dispenser di risorse COM+
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: Interfacce del dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a6ea5c5c09f67f86b42ebf5b881f1d19ad1501
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877501"
---
# <a name="com-resource-dispenser-interfaces"></a><span data-ttu-id="71264-103">Interfacce del dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="71264-103">COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="71264-104">I componenti dell'applicazione usano i distributori di risorse per accedere alle informazioni condivise.</span><span class="sxs-lookup"><span data-stu-id="71264-104">Application components use resource dispensers to access shared information.</span></span> <span data-ttu-id="71264-105">Le interfacce descritte nella tabella seguente forniscono informazioni di riferimento dettagliate per gli sviluppatori di distribuzioni di risorse.</span><span class="sxs-lookup"><span data-stu-id="71264-105">The interfaces described in the following table provide detailed reference information for developers of resource dispensers.</span></span>



| <span data-ttu-id="71264-106">Interfacce</span><span class="sxs-lookup"><span data-stu-id="71264-106">Interfaces</span></span>                                                | <span data-ttu-id="71264-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71264-107">Description</span></span>                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71264-108">**IDispenserDriver**</span><span class="sxs-lookup"><span data-stu-id="71264-108">**IDispenserDriver**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | <span data-ttu-id="71264-109">Questa interfaccia viene chiamata dal titolare del distributore di risorse per creare, integrare, valutare ed eliminare una risorsa.</span><span class="sxs-lookup"><span data-stu-id="71264-109">This interface is called by the resource dispenser holder to create, enlist, evaluate, and destroy a resource.</span></span><br/> |
| [<span data-ttu-id="71264-110">**IDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="71264-110">**IDispenserManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | <span data-ttu-id="71264-111">I dispenser di risorse usano questa interfaccia per connettersi al gestore del dispenser.</span><span class="sxs-lookup"><span data-stu-id="71264-111">Resource dispensers use this interface to connect to the dispenser manager.</span></span><br/>                                    |
| [<span data-ttu-id="71264-112">**IHolder**</span><span class="sxs-lookup"><span data-stu-id="71264-112">**IHolder**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | <span data-ttu-id="71264-113">Questa interfaccia viene utilizzata per preparare e gestire le risorse.</span><span class="sxs-lookup"><span data-stu-id="71264-113">This interface is used to prepare and handle resources.</span></span><br/>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="71264-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71264-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71264-115">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="71264-115">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="71264-116">Tipi utilizzati nelle interfacce del dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="71264-116">Types Used in COM+ Resource Dispenser Interfaces</span></span>](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




