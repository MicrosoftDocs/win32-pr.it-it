---
description: L'interfaccia IInstallationProgress definisce le proprietà seguenti.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: Proprietà di IInstallationProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbcdb162c544c81b96326ec7b2b7657d81538a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307646"
---
# <a name="iinstallationprogress-properties"></a><span data-ttu-id="932d1-103">Proprietà di IInstallationProgress</span><span class="sxs-lookup"><span data-stu-id="932d1-103">IInstallationProgress Properties</span></span>

<span data-ttu-id="932d1-104">L'interfaccia [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="932d1-104">The [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="932d1-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="932d1-105">Property</span></span>                                                                                   | <span data-ttu-id="932d1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="932d1-106">Description</span></span>                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="932d1-107">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="932d1-107">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | <span data-ttu-id="932d1-108">Ottiene un valore di indice in base zero che specifica l'aggiornamento attualmente in fase di installazione o disinstallazione quando sono stati selezionati più aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="932d1-108">Gets a zero-based index value that specifies the update that is currently being installed or uninstalled when multiple updates have been selected.</span></span> |
| [<span data-ttu-id="932d1-109">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="932d1-109">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="932d1-110">Ottiene l'avanzamento del processo di installazione o disinstallazione dell'aggiornamento corrente, come percentuale.</span><span class="sxs-lookup"><span data-stu-id="932d1-110">Gets how far the installation or uninstallation process for the current update has progressed, as a percentage.</span></span>                                    |
| [<span data-ttu-id="932d1-111">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="932d1-111">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | <span data-ttu-id="932d1-112">Ottiene la percentuale di avanzamento del processo di installazione o disinstallazione generale.</span><span class="sxs-lookup"><span data-stu-id="932d1-112">Gets how far the overall installation or uninstallation process has progressed, as a percentage.</span></span>                                                   |



 

 

 



