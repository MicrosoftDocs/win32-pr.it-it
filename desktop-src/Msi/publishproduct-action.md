---
description: L'azione PublishProduct gestisce l'annuncio delle informazioni sul prodotto con il sistema. Questa azione pubblica il prodotto se il prodotto è in modalità di annuncio o se è in corso l'installazione o la reinstallazione di una funzionalità.
ms.assetid: aba1baf2-d282-4f76-87aa-67188b779535
title: Azione PublishProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9edf95ccb736bb4a4388f36d87bfbfbe299573e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311726"
---
# <a name="publishproduct-action"></a><span data-ttu-id="251b7-104">Azione PublishProduct</span><span class="sxs-lookup"><span data-stu-id="251b7-104">PublishProduct Action</span></span>

<span data-ttu-id="251b7-105">L'azione PublishProduct gestisce l'annuncio delle informazioni sul prodotto con il sistema.</span><span class="sxs-lookup"><span data-stu-id="251b7-105">The PublishProduct action manages the advertisement of the product information with the system.</span></span> <span data-ttu-id="251b7-106">Questa azione pubblica il prodotto se il prodotto è in modalità di annuncio o se è in corso l'installazione o la reinstallazione di una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="251b7-106">This action publishes the product if the product is in advertise mode or if any feature is being installed or reinstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="251b7-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="251b7-107">Sequence Restrictions</span></span>

<span data-ttu-id="251b7-108">L'azione PublishProduct deve essere successiva all'azione [PublishFeatures](publishfeatures-action.md) .</span><span class="sxs-lookup"><span data-stu-id="251b7-108">The PublishProduct action must come after the [PublishFeatures](publishfeatures-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="251b7-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="251b7-109">ActionData Messages</span></span>



| <span data-ttu-id="251b7-110">Campo</span><span class="sxs-lookup"><span data-stu-id="251b7-110">Field</span></span> | <span data-ttu-id="251b7-111">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="251b7-111">Description of Action Data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="251b7-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="251b7-112">\[1\]</span></span> | <span data-ttu-id="251b7-113">Identificatore del prodotto pubblicizzato.</span><span class="sxs-lookup"><span data-stu-id="251b7-113">Identifier of advertised product.</span></span> |



 

 

 



