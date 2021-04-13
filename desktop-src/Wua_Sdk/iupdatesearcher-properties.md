---
description: L'interfaccia IUpdateSearcher definisce le proprietà seguenti.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Proprietà di IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/11/2021
ms.locfileid: "104354016"
---
# <a name="iupdatesearcher-properties"></a><span data-ttu-id="875fd-103">Proprietà di IUpdateSearcher</span><span class="sxs-lookup"><span data-stu-id="875fd-103">IUpdateSearcher Properties</span></span>

<span data-ttu-id="875fd-104">L'interfaccia [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="875fd-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following properties.</span></span>



| <span data-ttu-id="875fd-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="875fd-105">Property</span></span>                                                                                           | <span data-ttu-id="875fd-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="875fd-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="875fd-107">**CanAutomaticallyUpgradeService**</span><span class="sxs-lookup"><span data-stu-id="875fd-107">**CanAutomaticallyUpgradeService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | <span data-ttu-id="875fd-108">Ottiene e imposta un valore booleano che indica se le chiamate future ai metodi [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) e [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) generano un aggiornamento automatico a Windows Update Agent (WUA).</span><span class="sxs-lookup"><span data-stu-id="875fd-108">Gets and sets a Boolean value that indicates whether future calls to the [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) and [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) methods result in an automatic upgrade to Windows Update Agent (WUA).</span></span> |
| [<span data-ttu-id="875fd-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="875fd-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | <span data-ttu-id="875fd-110">Identifica l'applicazione client corrente.</span><span class="sxs-lookup"><span data-stu-id="875fd-110">Identifies the current client application.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="875fd-111">**IncludePotentiallySupersededUpdates**</span><span class="sxs-lookup"><span data-stu-id="875fd-111">**IncludePotentiallySupersededUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | <span data-ttu-id="875fd-112">Ottiene e imposta un valore booleano che indica se i risultati della ricerca includono gli aggiornamenti sostituiti da altri aggiornamenti nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="875fd-112">Gets and sets a Boolean value that indicates whether the search results include updates that are superseded by other updates in the search results.</span></span>                                                                                          |
| [<span data-ttu-id="875fd-113">**Online**</span><span class="sxs-lookup"><span data-stu-id="875fd-113">**Online**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | <span data-ttu-id="875fd-114">Ottiene e imposta un valore booleano che indica se [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) passa online per la ricerca degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="875fd-114">Gets and sets a Boolean value that indicates whether the [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) goes online to search for updates.</span></span>                                                                                                        |
| [<span data-ttu-id="875fd-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="875fd-115">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | <span data-ttu-id="875fd-116">Ottiene e imposta un sito in cui eseguire la ricerca quando il sito in cui eseguire la ricerca non è un sito Windows Update.</span><span class="sxs-lookup"><span data-stu-id="875fd-116">Gets and sets a site to search when the site to search is not a Windows Update site.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="875fd-117">**ServerSelection**</span><span class="sxs-lookup"><span data-stu-id="875fd-117">**ServerSelection**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | <span data-ttu-id="875fd-118">Ottiene e imposta un valore [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) che indica il server in cui cercare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="875fd-118">Gets and sets a [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) value that indicates the server to search for updates.</span></span>                                                                                                                            |




 

 

 



