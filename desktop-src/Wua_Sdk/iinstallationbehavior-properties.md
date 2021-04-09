---
description: L'interfaccia IInstallationBehavior definisce le proprietà seguenti.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Proprietà di IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966737"
---
# <a name="iinstallationbehavior-properties"></a><span data-ttu-id="7eeb3-103">Proprietà di IInstallationBehavior</span><span class="sxs-lookup"><span data-stu-id="7eeb3-103">IInstallationBehavior Properties</span></span>

<span data-ttu-id="7eeb3-104">L'interfaccia [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="7eeb3-104">The [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) interface defines the following properties.</span></span>



| <span data-ttu-id="7eeb3-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7eeb3-105">Property</span></span>                                                                                 | <span data-ttu-id="7eeb3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eeb3-106">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7eeb3-107">**CanRequestUserInput**</span><span class="sxs-lookup"><span data-stu-id="7eeb3-107">**CanRequestUserInput**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | <span data-ttu-id="7eeb3-108">Ottiene un valore booleano thast indica se l'installazione o la disinstallazione di un aggiornamento può richiedere l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7eeb3-108">Gets a Boolean value thast indicates whether the installation or uninstallation of an update can prompt for user input.</span></span>                                                        |
| [<span data-ttu-id="7eeb3-109">**Impatto**</span><span class="sxs-lookup"><span data-stu-id="7eeb3-109">**Impact**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | <span data-ttu-id="7eeb3-110">Ottiene un'enumerazione [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) che indica il modo in cui l'installazione o la disinstallazione dell'aggiornamento influiscono sul computer.</span><span class="sxs-lookup"><span data-stu-id="7eeb3-110">Gets an [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) enumeration that indicates how the installation or uninstallation of the update affects the computer.</span></span>                 |
| [<span data-ttu-id="7eeb3-111">**RebootBehavior**</span><span class="sxs-lookup"><span data-stu-id="7eeb3-111">**RebootBehavior**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | <span data-ttu-id="7eeb3-112">Ottiene un'enumerazione [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) che specifica il comportamento di riavvio che si verifica durante l'installazione o la disinstallazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7eeb3-112">Gets an [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) enumeration that specifies the restart behavior that occurs when you install or uninstall the update.</span></span> |
| [<span data-ttu-id="7eeb3-113">**RequiresNetworkConnectivity**</span><span class="sxs-lookup"><span data-stu-id="7eeb3-113">**RequiresNetworkConnectivity**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | <span data-ttu-id="7eeb3-114">Ottiene un valore booleano che indica se l'installazione o la disinstallazione di un aggiornamento richiede la connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="7eeb3-114">Gets a Boolean value that indicates whether the installation or uninstallation of an update requires network connectivity.</span></span>                                                     |



 

 

 



