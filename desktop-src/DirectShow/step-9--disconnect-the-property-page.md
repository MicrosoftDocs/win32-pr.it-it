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
# <a name="step-9-disconnect-the-property-page"></a>Passaggio 9. Disconnettere la pagina delle proprietà

Eseguire l'override del metodo [**CBasePropertyPage:: Disconnect**](cbasepropertypage-ondisconnect.md) per rilasciare tutte le interfacce ottenute nel metodo **OnConnect** . Inoltre, se l'utente omette la finestra delle proprietà senza eseguire il commit delle modifiche, è necessario ripristinare i valori originali se sono stati modificati. Non esiste alcun metodo "OnCancel" che viene chiamato quando l'utente Annulla, quindi è necessario tenere traccia del fatto che l'utente abbia chiamato **OnApplyChanges**. Questo esempio usa la \_ variabile m LVAL, descritta in precedenza:


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



Successivo: [passaggio 10. Supporto della registrazione COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



