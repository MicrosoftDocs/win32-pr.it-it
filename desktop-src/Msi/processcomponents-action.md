---
description: L'azione ProcessComponents registra e Annulla la registrazione dei componenti, dei percorsi chiave e dei client dei componenti.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Azione ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316254"
---
# <a name="processcomponents-action"></a><span data-ttu-id="e2800-103">Azione ProcessComponents</span><span class="sxs-lookup"><span data-stu-id="e2800-103">ProcessComponents Action</span></span>

<span data-ttu-id="e2800-104">L'azione ProcessComponents registra e Annulla la registrazione dei componenti, dei percorsi chiave e dei client dei componenti.</span><span class="sxs-lookup"><span data-stu-id="e2800-104">The ProcessComponents action registers and unregisters components, their key paths, and the component clients.</span></span> <span data-ttu-id="e2800-105">L'azione ProcessComponents esegue una query sulla colonna di percorso della [tabella dei componenti](component-table.md) per determinare i percorsi della colonna.</span><span class="sxs-lookup"><span data-stu-id="e2800-105">The ProcessComponents action queries the KeyPath column of the [Component table](component-table.md) to determine keypaths.</span></span> <span data-ttu-id="e2800-106">Questa registrazione viene utilizzata da [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) per restituire il percorso di un componente per un client del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e2800-106">This registration is used by [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to return the path of a component for a product client.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e2800-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="e2800-107">Sequence Restrictions</span></span>

<span data-ttu-id="e2800-108">L'azione ProcessComponents deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e2800-108">The ProcessComponents action must come after the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e2800-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="e2800-109">ActionData Messages</span></span>

<span data-ttu-id="e2800-110">Per ogni componente registrato.</span><span class="sxs-lookup"><span data-stu-id="e2800-110">For each component being registered.</span></span>



| <span data-ttu-id="e2800-111">Campo</span><span class="sxs-lookup"><span data-stu-id="e2800-111">Field</span></span> | <span data-ttu-id="e2800-112">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="e2800-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="e2800-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e2800-113">\[1\]</span></span> | <span data-ttu-id="e2800-114">ProductId</span><span class="sxs-lookup"><span data-stu-id="e2800-114">ProductId</span></span>                       |
| <span data-ttu-id="e2800-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e2800-115">\[2\]</span></span> | <span data-ttu-id="e2800-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e2800-116">ComponentId</span></span>                     |
| <span data-ttu-id="e2800-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="e2800-117">\[3\]</span></span> | <span data-ttu-id="e2800-118">Percorso della chiave per il componente.</span><span class="sxs-lookup"><span data-stu-id="e2800-118">The key path for the component.</span></span> |



 

<span data-ttu-id="e2800-119">Per ogni componente di cui viene annullata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="e2800-119">For each component being unregistered.</span></span>



| <span data-ttu-id="e2800-120">Campo</span><span class="sxs-lookup"><span data-stu-id="e2800-120">Field</span></span> | <span data-ttu-id="e2800-121">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="e2800-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="e2800-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e2800-122">\[1\]</span></span> | <span data-ttu-id="e2800-123">ProductId</span><span class="sxs-lookup"><span data-stu-id="e2800-123">ProductId</span></span>                  |
| <span data-ttu-id="e2800-124">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e2800-124">\[2\]</span></span> | <span data-ttu-id="e2800-125">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e2800-125">ComponentId</span></span>                |



 

 

 



