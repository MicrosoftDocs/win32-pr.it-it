---
description: Passaggio 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Passaggio 9. Disconnettere la pagina delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316313"
---
# <a name="step-9-disconnect-the-property-page"></a><span data-ttu-id="cf543-104">Passaggio 9.</span><span class="sxs-lookup"><span data-stu-id="cf543-104">Step 9.</span></span> <span data-ttu-id="cf543-105">Disconnettere la pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="cf543-105">Disconnect the Property Page</span></span>

<span data-ttu-id="cf543-106">Eseguire l'override del metodo [**CBasePropertyPage:: Disconnect**](cbasepropertypage-ondisconnect.md) per rilasciare tutte le interfacce ottenute nel metodo **OnConnect** .</span><span class="sxs-lookup"><span data-stu-id="cf543-106">Override the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method to release any interfaces that you obtained in the **OnConnect** method.</span></span> <span data-ttu-id="cf543-107">Inoltre, se l'utente omette la finestra delle proprietà senza eseguire il commit delle modifiche, è necessario ripristinare i valori originali se sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="cf543-107">Also, if the user dismisses the property sheet without committing the changes, you should restore the original values if they have changed.</span></span> <span data-ttu-id="cf543-108">Non esiste alcun metodo "OnCancel" che viene chiamato quando l'utente Annulla, quindi è necessario tenere traccia del fatto che l'utente abbia chiamato **OnApplyChanges**.</span><span class="sxs-lookup"><span data-stu-id="cf543-108">There is no "OnCancel" method that gets called when the user cancels, so you need to keep track of whether the user has called **OnApplyChanges**.</span></span> <span data-ttu-id="cf543-109">Questo esempio usa la \_ variabile m LVAL, descritta in precedenza:</span><span class="sxs-lookup"><span data-stu-id="cf543-109">This example uses the m\_lVal variable, described earlier:</span></span>


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



<span data-ttu-id="cf543-110">Successivo: [passaggio 10. Supporto della registrazione COM](step-10--support-com-registration.md)</span><span class="sxs-lookup"><span data-stu-id="cf543-110">Next: [Step 10. Support COM Registration](step-10--support-com-registration.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf543-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf543-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf543-112">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="cf543-112">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



