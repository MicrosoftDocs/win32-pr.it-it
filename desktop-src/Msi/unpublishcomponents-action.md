---
description: L'azione UnpublishComponents gestisce l'unadvertising dei componenti elencati nella tabella PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Azione UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104401918"
---
# <a name="unpublishcomponents-action"></a><span data-ttu-id="5c3b3-103">Azione UnpublishComponents</span><span class="sxs-lookup"><span data-stu-id="5c3b3-103">UnpublishComponents Action</span></span>

<span data-ttu-id="5c3b3-104">L'azione UnpublishComponents gestisce l'unadvertising dei componenti elencati nella tabella PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="5c3b3-104">The UnpublishComponents action manages the unadvertisement of components listed in the PublishComponent table.</span></span> <span data-ttu-id="5c3b3-105">Si tratta di componenti che possono avere errori in altri prodotti.</span><span class="sxs-lookup"><span data-stu-id="5c3b3-105">These are components that may be faulted in by other products.</span></span> <span data-ttu-id="5c3b3-106">Questa azione consente di rimuovere informazioni sui componenti pubblicati dalla [tabella PublishComponent](publishcomponent-table.md) per cui è attualmente selezionata la funzionalità corrispondente per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="5c3b3-106">This action removes information about published components from the [PublishComponent table](publishcomponent-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5c3b3-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="5c3b3-107">Sequence Restrictions</span></span>

<span data-ttu-id="5c3b3-108">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="5c3b3-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5c3b3-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="5c3b3-109">ActionData Messages</span></span>



| <span data-ttu-id="5c3b3-110">Campo</span><span class="sxs-lookup"><span data-stu-id="5c3b3-110">Field</span></span> | <span data-ttu-id="5c3b3-111">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="5c3b3-111">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="5c3b3-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5c3b3-112">\[1\]</span></span> | <span data-ttu-id="5c3b3-113">GUID che rappresenta l'ID componente di una funzionalità annunciata.</span><span class="sxs-lookup"><span data-stu-id="5c3b3-113">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="5c3b3-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="5c3b3-114">\[2\]</span></span> | <span data-ttu-id="5c3b3-115">Qualificatore dell'ID componente.</span><span class="sxs-lookup"><span data-stu-id="5c3b3-115">Qualifier of the component ID.</span></span>                               |



 

