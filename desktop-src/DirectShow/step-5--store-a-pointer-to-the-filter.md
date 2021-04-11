---
description: Passaggio 5.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Passaggio 5. Archiviare un puntatore al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232985"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="c7251-104">Passaggio 5.</span><span class="sxs-lookup"><span data-stu-id="c7251-104">Step 5.</span></span> <span data-ttu-id="c7251-105">Archiviare un puntatore al filtro</span><span class="sxs-lookup"><span data-stu-id="c7251-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="c7251-106">Eseguire l'override del metodo [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) per archiviare un puntatore al filtro.</span><span class="sxs-lookup"><span data-stu-id="c7251-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="c7251-107">Nell'esempio seguente viene eseguita una query sul parametro *punk* per l'interfaccia ISaturation personalizzata del filtro:</span><span class="sxs-lookup"><span data-stu-id="c7251-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


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



<span data-ttu-id="c7251-108">[Passaggio 6: Inizializzare la finestra di dialogo](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c7251-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7251-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7251-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7251-110">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="c7251-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



