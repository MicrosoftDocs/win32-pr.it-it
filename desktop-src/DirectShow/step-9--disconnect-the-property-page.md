---
description: Passaggio 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Passaggio 9. Disconnettere la pagina delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf4bcb670b8a8f29334f7ecd41ebba37a915f724be70e5dbbbfd7abea9730be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526082"
---
# <a name="step-9-disconnect-the-property-page"></a>Passaggio 9. Disconnettere la pagina delle proprietà

Eseguire [**l'override del metodo CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) per rilasciare tutte le interfacce ottenute nel **metodo OnConnect.** Inoltre, se l'utente chiude la finestra delle proprietà senza eseguire il commit delle modifiche, è necessario ripristinare i valori originali se sono stati modificati. Non esiste alcun metodo "OnCancel" che viene chiamato quando l'utente annulla, pertanto è necessario tenere traccia del fatto che l'utente abbia chiamato **OnApplyChanges.** Questo esempio usa la variabile m \_ lVal, descritta in precedenza:


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



Passaggio [10. Supporto della registrazione COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



