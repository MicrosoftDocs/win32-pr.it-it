---
description: L'azione PublishComponents gestisce l'annuncio dei componenti dalla tabella PublishComponent.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: Azione PublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c8967e737193922a9dbc3d9e03bc95131d5a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881497"
---
# <a name="publishcomponents-action"></a><span data-ttu-id="a36c9-103">Azione PublishComponents</span><span class="sxs-lookup"><span data-stu-id="a36c9-103">PublishComponents Action</span></span>

<span data-ttu-id="a36c9-104">L'azione PublishComponents gestisce l'annuncio dei componenti dalla tabella [PublishComponent](publishcomponent-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a36c9-104">The PublishComponents action manages the advertisement of the components from the [PublishComponent](publishcomponent-table.md) table.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a36c9-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="a36c9-105">Sequence Restrictions</span></span>

<span data-ttu-id="a36c9-106">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="a36c9-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a36c9-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="a36c9-107">ActionData Messages</span></span>



| <span data-ttu-id="a36c9-108">Campo</span><span class="sxs-lookup"><span data-stu-id="a36c9-108">Field</span></span> | <span data-ttu-id="a36c9-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="a36c9-109">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="a36c9-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a36c9-110">\[1\]</span></span> | <span data-ttu-id="a36c9-111">GUID che rappresenta l'ID componente di una funzionalità annunciata.</span><span class="sxs-lookup"><span data-stu-id="a36c9-111">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="a36c9-112">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a36c9-112">\[2\]</span></span> | <span data-ttu-id="a36c9-113">Qualificatore dell'ID componente.</span><span class="sxs-lookup"><span data-stu-id="a36c9-113">Qualifier of component ID.</span></span>                                   |



 

## <a name="remarks"></a><span data-ttu-id="a36c9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a36c9-114">Remarks</span></span>

<span data-ttu-id="a36c9-115">L'azione PublishComponents pubblica tutti i componenti dalla tabella PublishComponents che appartengono alle funzionalità selezionate per l'annuncio o l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a36c9-115">The PublishComponents action publishes all of the components from the PublishComponents table that belong to features that have been selected for advertisement or installation.</span></span>

 

 



