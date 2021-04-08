---
title: Interfacce NDF
description: Le interfacce seguenti possono essere utilizzate per estendere la funzionalità delle classi helper Microsoft identificate come estendibili.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043987"
---
# <a name="ndf-interfaces"></a><span data-ttu-id="8278c-103">Interfacce NDF</span><span class="sxs-lookup"><span data-stu-id="8278c-103">NDF Interfaces</span></span>

<span data-ttu-id="8278c-104">Le interfacce seguenti possono essere utilizzate per estendere la funzionalità delle classi helper Microsoft identificate come estendibili.</span><span class="sxs-lookup"><span data-stu-id="8278c-104">The following interfaces can be used to extend the functionality of Microsoft Helper Classes that are identified as extensible.</span></span> <span data-ttu-id="8278c-105">Anche se questa funzionalità non è necessaria per la maggior parte delle applicazioni, può fornire diagnosi e soluzioni più specifiche in alcuni casi.</span><span class="sxs-lookup"><span data-stu-id="8278c-105">Although this functionality is not required for most applications, it can provide more specific diagnoses and resolutions in some cases.</span></span>

> [!Note]  
> <span data-ttu-id="8278c-106">Queste interfacce e i relativi metodi associati sono destinate agli sviluppatori che implementano le proprie classi helper di terze parti che estendono la funzionalità NDF.</span><span class="sxs-lookup"><span data-stu-id="8278c-106">These interfaces and their associated methods are for developers implementing their own third party helper classes that extend NDF functionality.</span></span>

 



| <span data-ttu-id="8278c-107">Interface Name (Nome interfaccia)</span><span class="sxs-lookup"><span data-stu-id="8278c-107">Interface Name</span></span>                                                 | <span data-ttu-id="8278c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8278c-108">Description</span></span>                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8278c-109">**INetDiagHelper**</span><span class="sxs-lookup"><span data-stu-id="8278c-109">**INetDiagHelper**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | <span data-ttu-id="8278c-110">Chiamato da NDF per la maggior parte delle attività che si verificano durante una diagnosi.</span><span class="sxs-lookup"><span data-stu-id="8278c-110">Called by the NDF for most activities that occur during a diagnosis.</span></span>                                                     |
| [<span data-ttu-id="8278c-111">**INetDiagHelperEx**</span><span class="sxs-lookup"><span data-stu-id="8278c-111">**INetDiagHelperEx**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | <span data-ttu-id="8278c-112">Chiamato da NDF per acquisire e fornire informazioni associate a diagnosi e risoluzione dei problemi relativi alla rete.</span><span class="sxs-lookup"><span data-stu-id="8278c-112">Called by the NDF to capture and provide information associated with diagnoses and resolution of network-related issues.</span></span> |
| [<span data-ttu-id="8278c-113">**INetDiagHelperInfo**</span><span class="sxs-lookup"><span data-stu-id="8278c-113">**INetDiagHelperInfo**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | <span data-ttu-id="8278c-114">Chiamato da NDF per verificare che disponga di informazioni obbligatorie</span><span class="sxs-lookup"><span data-stu-id="8278c-114">Called by the NDF to validate that it has required information</span></span>                                                           |
| [<span data-ttu-id="8278c-115">**INetDiagHelperUtilFactory**</span><span class="sxs-lookup"><span data-stu-id="8278c-115">**INetDiagHelperUtilFactory**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | <span data-ttu-id="8278c-116">Riservato per l'utilizzo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="8278c-116">Reserved for system use.</span></span>                                                                                                 |



 

 

 




