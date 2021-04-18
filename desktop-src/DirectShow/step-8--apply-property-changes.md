---
description: Passaggio 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Passaggio 8. Applicare le modifiche alle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316311"
---
# <a name="step-8-apply-property-changes"></a><span data-ttu-id="59a47-104">Passaggio 8.</span><span class="sxs-lookup"><span data-stu-id="59a47-104">Step 8.</span></span> <span data-ttu-id="59a47-105">Applicare le modifiche alle proprietà</span><span class="sxs-lookup"><span data-stu-id="59a47-105">Apply Property Changes</span></span>

<span data-ttu-id="59a47-106">Eseguire l'override del metodo [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) per eseguire il commit di tutte le modifiche alle proprietà.</span><span class="sxs-lookup"><span data-stu-id="59a47-106">Override the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method to commit any property changes.</span></span> <span data-ttu-id="59a47-107">In questo esempio la variabile m \_ lNewVal viene aggiornata ogni volta che l'utente scorre la barra del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="59a47-107">In this example, the m\_lNewVal variable is updated whenever the user scrolls the slider bar.</span></span> <span data-ttu-id="59a47-108">Il metodo **OnApplyChanges** copia questo valore nella variabile m \_ LVAL, sovrascrivendo il valore originale:</span><span class="sxs-lookup"><span data-stu-id="59a47-108">The **OnApplyChanges** method copies this value into the m\_lVal variable, overwriting the original value:</span></span>


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



<span data-ttu-id="59a47-109">Successivo: [passaggio 9. Disconnettere la pagina delle proprietà](step-9--disconnect-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="59a47-109">Next: [Step 9. Disconnect the Property Page](step-9--disconnect-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59a47-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59a47-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59a47-111">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="59a47-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



