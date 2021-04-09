---
description: L'interfaccia IUpdateInstaller definisce le proprietà seguenti.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Proprietà di IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879438"
---
# <a name="iupdateinstaller-properties"></a><span data-ttu-id="45bab-103">Proprietà di IUpdateInstaller</span><span class="sxs-lookup"><span data-stu-id="45bab-103">IUpdateInstaller Properties</span></span>

<span data-ttu-id="45bab-104">L'interfaccia [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="45bab-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following properties.</span></span>



| <span data-ttu-id="45bab-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45bab-105">Property</span></span>                                                                                      | <span data-ttu-id="45bab-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45bab-106">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45bab-107">**AllowSourcePrompts**</span><span class="sxs-lookup"><span data-stu-id="45bab-107">**AllowSourcePrompts**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | <span data-ttu-id="45bab-108">Ottiene e imposta un valore booleano che indica se visualizzare le richieste di origine all'utente durante l'installazione degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="45bab-108">Gets and sets a Boolean value that indicates whether to show source prompts to the user when installing the updates.</span></span>                  |
| [<span data-ttu-id="45bab-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="45bab-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | <span data-ttu-id="45bab-110">Ottiene e imposta l'applicazione client corrente.</span><span class="sxs-lookup"><span data-stu-id="45bab-110">Gets and sets the current client application.</span></span>                                                                                         |
| [<span data-ttu-id="45bab-111">**Della proprietà IsBusy**</span><span class="sxs-lookup"><span data-stu-id="45bab-111">**IsBusy**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | <span data-ttu-id="45bab-112">Ottiene un valore booleano che indica se è in corso un'installazione o una disinstallazione di un computer in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="45bab-112">Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.</span></span>        |
| [<span data-ttu-id="45bab-113">**IsForced**</span><span class="sxs-lookup"><span data-stu-id="45bab-113">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | <span data-ttu-id="45bab-114">Ottiene o imposta un valore booleano che indica se forzare l'installazione o la disinstallazione di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="45bab-114">Gets or sets a Boolean value that indicates whether to forcibly install or uninstall an update.</span></span>                                       |
| [<span data-ttu-id="45bab-115">**ParentHwnd**</span><span class="sxs-lookup"><span data-stu-id="45bab-115">**ParentHwnd**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | <span data-ttu-id="45bab-116">Ottiene e imposta un handle per la finestra padre che può contenere una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="45bab-116">Gets and sets a handle to the parent window that can contain a dialog box.</span></span>                                                            |
| [<span data-ttu-id="45bab-117">**ParentWindow**</span><span class="sxs-lookup"><span data-stu-id="45bab-117">**ParentWindow**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | <span data-ttu-id="45bab-118">Ottiene e imposta l'interfaccia che rappresenta la finestra padre che può contenere una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="45bab-118">Gets and sets the interface that represents the parent window that can contain a dialog box.</span></span>                                          |
| [<span data-ttu-id="45bab-119">**RebootRequiredBeforeInstallation**</span><span class="sxs-lookup"><span data-stu-id="45bab-119">**RebootRequiredBeforeInstallation**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | <span data-ttu-id="45bab-120">Ottiene un valore booleano che indica se è necessario riavviare il sistema prima di installare o disinstallare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="45bab-120">Gets a Boolean value that indicates whether a system restart is required before installing or uninstalling updates.</span></span>                   |
| [<span data-ttu-id="45bab-121">**Aggiornamenti**</span><span class="sxs-lookup"><span data-stu-id="45bab-121">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | <span data-ttu-id="45bab-122">Ottiene e imposta un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati per l'installazione o la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="45bab-122">Gets and sets an interface that contains a read-only collection of the updates that are specified for installation or uninstallation.</span></span> |



 

 

 



