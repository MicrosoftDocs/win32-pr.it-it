---
description: L'interfaccia IInstallationJob definisce le proprietà seguenti.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Proprietà di IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752095"
---
# <a name="iinstallationjob-properties"></a><span data-ttu-id="7bc46-103">Proprietà di IInstallationJob</span><span class="sxs-lookup"><span data-stu-id="7bc46-103">IInstallationJob Properties</span></span>

<span data-ttu-id="7bc46-104">L'interfaccia [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="7bc46-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following properties.</span></span>



| <span data-ttu-id="7bc46-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7bc46-105">Property</span></span>                                            | <span data-ttu-id="7bc46-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bc46-106">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bc46-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="7bc46-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | <span data-ttu-id="7bc46-108">Ottiene l'oggetto di stato specifico del chiamante passato al metodo [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .</span><span class="sxs-lookup"><span data-stu-id="7bc46-108">Gets the caller-specific state object that is passed to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method.</span></span>               |
| [<span data-ttu-id="7bc46-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="7bc46-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | <span data-ttu-id="7bc46-110">Ottiene un valore che indica se una chiamata al metodo [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) è stata elaborata completamente.</span><span class="sxs-lookup"><span data-stu-id="7bc46-110">Gets a value that indicates whether a call to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method is completely processed.</span></span> |
| [<span data-ttu-id="7bc46-111">**Aggiornamenti**</span><span class="sxs-lookup"><span data-stu-id="7bc46-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | <span data-ttu-id="7bc46-112">Ottiene un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati durante l'installazione o la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="7bc46-112">Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.</span></span>                                                                                                        |



 

 

 



