---
description: L'interfaccia ISearchJob definisce le proprietà seguenti.
ms.assetid: 9e1675e9-fe40-4209-aba9-1cabb4f3ea4c
title: Proprietà di ISearchJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c49a5af7435819750451c89ca68f976d76f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129638"
---
# <a name="isearchjob-properties"></a><span data-ttu-id="fce11-103">Proprietà di ISearchJob</span><span class="sxs-lookup"><span data-stu-id="fce11-103">ISearchJob Properties</span></span>

<span data-ttu-id="fce11-104">L'interfaccia [**ISearchJob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="fce11-104">The [**ISearchJob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) interface defines the following properties.</span></span>



| <span data-ttu-id="fce11-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fce11-105">Property</span></span>                                      | <span data-ttu-id="fce11-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fce11-106">Description</span></span>                                                                                                                                                 |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fce11-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="fce11-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_asyncstate)   | <span data-ttu-id="fce11-108">Ottiene l'oggetto di stato specifico del chiamante passato al metodo [**IUpdateSearch. BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) .</span><span class="sxs-lookup"><span data-stu-id="fce11-108">Gets the caller-specific state object that is passed to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method.</span></span>                         |
| [<span data-ttu-id="fce11-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="fce11-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_iscompleted) | <span data-ttu-id="fce11-110">Ottiene un valore booleano che indica se la chiamata al metodo [**IUpdateSearch. BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) è stata elaborata completamente.</span><span class="sxs-lookup"><span data-stu-id="fce11-110">Gets a Boolean value that indicates whether the call to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method is completely processed.</span></span> |



 

 

 



