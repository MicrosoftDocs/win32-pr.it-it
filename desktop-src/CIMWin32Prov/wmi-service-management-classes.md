---
description: Le classi di gestione del servizio WMI vengono utilizzate per gestire il servizio WMI stesso e non il sistema del computer o la rete aziendale. La gestione di WMI comprende sia la configurazione del servizio WMI che la gestione delle operazioni WMI.
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: Classi di gestione del servizio WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126069"
---
# <a name="wmi-service-management-classes"></a><span data-ttu-id="f4d60-104">Classi di gestione del servizio WMI</span><span class="sxs-lookup"><span data-stu-id="f4d60-104">WMI Service Management Classes</span></span>

<span data-ttu-id="f4d60-105">Le classi di gestione del servizio WMI vengono utilizzate per gestire il servizio WMI stesso e non il sistema del computer o la rete aziendale.</span><span class="sxs-lookup"><span data-stu-id="f4d60-105">WMI service management classes are used to manage the WMI service itself and not the computer system or enterprise network.</span></span> <span data-ttu-id="f4d60-106">La gestione di WMI comprende sia la configurazione del servizio WMI che la gestione delle operazioni WMI.</span><span class="sxs-lookup"><span data-stu-id="f4d60-106">Managing WMI encompasses both configuring the WMI service and managing WMI operations.</span></span>

<span data-ttu-id="f4d60-107">La categoria Gestione del servizio WMI include le sottocategorie di classi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4d60-107">The WMI Service Management category includes the following subcategories of classes:</span></span>

-   [<span data-ttu-id="f4d60-108">Classi di configurazione WMI</span><span class="sxs-lookup"><span data-stu-id="f4d60-108">WMI configuration classes</span></span>](#wmi-configuration-classes)
-   [<span data-ttu-id="f4d60-109">Classi di gestione WMI</span><span class="sxs-lookup"><span data-stu-id="f4d60-109">WMI management classes</span></span>](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a><span data-ttu-id="f4d60-110">Classi di configurazione WMI</span><span class="sxs-lookup"><span data-stu-id="f4d60-110">WMI Configuration Classes</span></span>

<span data-ttu-id="f4d60-111">La classe di configurazione WMI deriva i metodi che configurano il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="f4d60-111">The WMI Configuration class derives methods that configure the WMI service.</span></span>

<span data-ttu-id="f4d60-112">Di seguito è riportata una tabella delle classi di configurazione WMI.</span><span class="sxs-lookup"><span data-stu-id="f4d60-112">The following is a table of WMI configuration classes.</span></span>



| <span data-ttu-id="f4d60-113">Classe</span><span class="sxs-lookup"><span data-stu-id="f4d60-113">Class</span></span>                                                             | <span data-ttu-id="f4d60-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4d60-114">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f4d60-115">**\_MethodParameterClass Win32**</span><span class="sxs-lookup"><span data-stu-id="f4d60-115">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md) | <span data-ttu-id="f4d60-116">Classe di base astratta che implementa i parametri del metodo derivati da questa classe.</span><span class="sxs-lookup"><span data-stu-id="f4d60-116">Abstract, base class that implements method parameters derived from this class.</span></span> |



 

## <a name="wmi-management-classes"></a><span data-ttu-id="f4d60-117">Classi di gestione WMI</span><span class="sxs-lookup"><span data-stu-id="f4d60-117">WMI Management Classes</span></span>

<span data-ttu-id="f4d60-118">Le classi di gestione WMI rappresentano i parametri operativi per il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="f4d60-118">The WMI management classes represent operational parameters for the WMI service.</span></span>

<span data-ttu-id="f4d60-119">Di seguito è riportata una tabella delle classi di gestione WMI.</span><span class="sxs-lookup"><span data-stu-id="f4d60-119">The following is a table of WMI management classes.</span></span>



| <span data-ttu-id="f4d60-120">Classe</span><span class="sxs-lookup"><span data-stu-id="f4d60-120">Class</span></span>                                                       | <span data-ttu-id="f4d60-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4d60-121">Description</span></span>                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4d60-122">**\_WMISetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f4d60-122">**Win32\_WMISetting**</span></span>](win32-wmisetting.md)               | <span data-ttu-id="f4d60-123">Contiene i parametri operativi per il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="f4d60-123">Contains the operational parameters for the WMI service.</span></span>                                      |
| [<span data-ttu-id="f4d60-124">**\_WMIElementSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f4d60-124">**Win32\_WMIElementSetting**</span></span>](win32-wmielementsetting.md) | <span data-ttu-id="f4d60-125">Associazione tra un servizio in esecuzione nel sistema Windows e le impostazioni WMI che può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f4d60-125">Association between a service running in the Windows system, and the WMI settings it can use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f4d60-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4d60-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4d60-127">Classi Win32</span><span class="sxs-lookup"><span data-stu-id="f4d60-127">Win32 Classes</span></span>](./win32-provider.md)
</dt> </dl>

 

 
