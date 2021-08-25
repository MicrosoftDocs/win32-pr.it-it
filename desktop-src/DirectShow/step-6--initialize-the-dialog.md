---
description: Eseguire l'override del metodo CBasePropertyPage::OnActivate per inizializzare la finestra di dialogo come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Passaggio 6. Inizializzare la finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2ac2dbc4e8ed59317db3db46079b087e4afcf0fa8dce315aa2a0cbd45d502a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102311"
---
# <a name="step-6-initialize-the-dialog"></a>Passaggio 6. Inizializzare la finestra di dialogo

Eseguire [**l'override del metodo CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) per inizializzare la finestra di dialogo. In questo esempio la pagina delle proprietà usa un controllo dispositivo di scorrimento, quindi il primo passaggio in **OnActivate** consiste nell'inizializzare la libreria di controlli comune. Il metodo inizializza quindi il controllo dispositivo di scorrimento usando il valore corrente della proprietà di saturazione del filtro:


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



Successivo: [Passaggio 7. Gestire i messaggi della finestra](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà Filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



