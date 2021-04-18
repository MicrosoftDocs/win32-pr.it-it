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
# <a name="step-8-apply-property-changes"></a>Passaggio 8. Applicare le modifiche alle proprietà

Eseguire l'override del metodo [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) per eseguire il commit di tutte le modifiche alle proprietà. In questo esempio la variabile m \_ lNewVal viene aggiornata ogni volta che l'utente scorre la barra del dispositivo di scorrimento. Il metodo **OnApplyChanges** copia questo valore nella variabile m \_ LVAL, sovrascrivendo il valore originale:


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Successivo: [passaggio 9. Disconnettere la pagina delle proprietà](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



