---
description: Eseguire l'override del metodo CBasePropertyPage::OnActivate per inizializzare la finestra di dialogo durante la creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Passaggio 6. Inizializzare il dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbdf18e272ac548227626bc9da4f992786a4ab3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404494"
---
# <a name="step-6-initialize-the-dialog"></a><span data-ttu-id="d5b2d-104">Passaggio 6.</span><span class="sxs-lookup"><span data-stu-id="d5b2d-104">Step 6.</span></span> <span data-ttu-id="d5b2d-105">Inizializzare il dialogo</span><span class="sxs-lookup"><span data-stu-id="d5b2d-105">Initialize the Dialog</span></span>

<span data-ttu-id="d5b2d-106">Eseguire [**l'override del metodo CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) per inizializzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="d5b2d-106">Override the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method to initialize the dialog.</span></span> <span data-ttu-id="d5b2d-107">In questo esempio la pagina delle proprietà usa un dispositivo di scorrimento, quindi il primo passaggio in **OnActivate** consiste nell'inizializzare la libreria di controlli comune.</span><span class="sxs-lookup"><span data-stu-id="d5b2d-107">In this example, the property page uses a slider control, so the first step in **OnActivate** is to initialize the common control library.</span></span> <span data-ttu-id="d5b2d-108">Il metodo inizializza quindi il dispositivo di scorrimento usando il valore corrente della proprietà di saturazione del filtro:</span><span class="sxs-lookup"><span data-stu-id="d5b2d-108">The method then initializes the slider control using the current value of the filter's saturation property:</span></span>


```C++
HRESULT CGrayProp::OnActivate(void)
{
    INITCOMMONCONTROLSEX icc;
    icc.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icc.dwICC = ICC_BAR_CLASSES;
    if (InitCommonControlsEx(&icc) == FALSE)
    {
        return E_FAIL;
    }

    ASSERT(m_pGray != NULL);
    HRESULT hr = m_pGray->GetSaturation(&m_lVal);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0,
            MAKELONG(SATURATION_MIN, SATURATION_MAX));

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 
            (SATURATION_MAX - SATURATION_MIN) / 10, 0);

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lVal);
    }
    return hr;
}
```



<span data-ttu-id="d5b2d-109">Passaggio [successivo: Passaggio 7. Gestire i messaggi della finestra](step-7--handle-window-messages.md)</span><span class="sxs-lookup"><span data-stu-id="d5b2d-109">Next: [Step 7. Handle Window Messages](step-7--handle-window-messages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5b2d-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5b2d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5b2d-111">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="d5b2d-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



