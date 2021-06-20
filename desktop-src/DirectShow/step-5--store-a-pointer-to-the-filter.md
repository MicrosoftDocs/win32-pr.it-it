---
description: Archiviare un puntatore a un filtro come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Passaggio 5. Archiviare un puntatore al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406794"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="98c87-104">Passaggio 5.</span><span class="sxs-lookup"><span data-stu-id="98c87-104">Step 5.</span></span> <span data-ttu-id="98c87-105">Archiviare un puntatore al filtro</span><span class="sxs-lookup"><span data-stu-id="98c87-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="98c87-106">Eseguire [**l'override del metodo CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) per archiviare un puntatore al filtro.</span><span class="sxs-lookup"><span data-stu-id="98c87-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="98c87-107">L'esempio seguente esegue *una query sul parametro pUnk* per l'interfaccia ISaturation personalizzata del filtro:</span><span class="sxs-lookup"><span data-stu-id="98c87-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



<span data-ttu-id="98c87-108">Passaggio [successivo: Passaggio 6. Inizializzare la finestra di dialogo](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="98c87-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="98c87-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="98c87-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98c87-110">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="98c87-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



