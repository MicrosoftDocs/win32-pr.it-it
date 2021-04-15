---
title: CPROVCF. CPP
description: Nel componente provider di esempio, un esempio di codice dell'oggetto provider ADs class factory codice si trova in cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470814"
---
# <a name="cprovcfcpp"></a><span data-ttu-id="acec2-103">CPROVCF. CPP</span><span class="sxs-lookup"><span data-stu-id="acec2-103">CPROVCF.CPP</span></span>

<span data-ttu-id="acec2-104">Nel componente provider di esempio, un esempio di codice dell'oggetto provider ADs class factory codice si trova in cprovcf. cpp.</span><span class="sxs-lookup"><span data-stu-id="acec2-104">In the example provider component, one code example of the ADs provider object class factory code is in cprovcf.cpp.</span></span> <span data-ttu-id="acec2-105">Il componente provider non crea mai direttamente un'istanza di questo oggetto in un momento diverso da quello in cui l'oggetto viene creato automaticamente durante le operazioni di associazione in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o nella funzione interna del Visual Basic metodo **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="acec2-105">The provider component never directly creates an instance of this object at any time other than when the object is created automatically during the binding operations in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or the internal function in the Visual Basic method **GetObject**.</span></span> <span data-ttu-id="acec2-106">Il metodo supportato è elencato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="acec2-106">The supported method is listed in the following table.</span></span>



| <span data-ttu-id="acec2-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="acec2-107">Method</span></span>                                  | <span data-ttu-id="acec2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acec2-108">Description</span></span>                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="acec2-109">**CSampleDSProviderCF:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="acec2-109">**CSampleDSProviderCF::CreateInstance**</span></span> | <span data-ttu-id="acec2-110">Crea un'istanza della class factory per l'oggetto provider ADS.</span><span class="sxs-lookup"><span data-stu-id="acec2-110">Creates an instance of the class factory for the ADS provider object.</span></span> |



 

 

 




