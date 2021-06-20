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
# <a name="step-6-initialize-the-dialog"></a>Passaggio 6. Inizializzare il dialogo

Eseguire [**l'override del metodo CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) per inizializzare la finestra di dialogo. In questo esempio la pagina delle proprietà usa un dispositivo di scorrimento, quindi il primo passaggio in **OnActivate** consiste nell'inizializzare la libreria di controlli comune. Il metodo inizializza quindi il dispositivo di scorrimento usando il valore corrente della proprietà di saturazione del filtro:


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



Passaggio [successivo: Passaggio 7. Gestire i messaggi della finestra](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



