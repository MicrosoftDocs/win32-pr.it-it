---
description: Passaggio 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Passaggio 8. Applicare modifiche alle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2292d9f294711129b2edba50ef6fb623d767dfba4122295222d08eb1ad21dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652057"
---
# <a name="step-8-apply-property-changes"></a>Passaggio 8. Applicare modifiche alle proprietà

Eseguire [**l'override del metodo CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) per eseguire il commit delle modifiche alle proprietà. In questo esempio la variabile m lNewVal viene aggiornata ogni volta che l'utente scorre la \_ barra del dispositivo di scorrimento. Il **metodo OnApplyChanges** copia questo valore nella variabile m \_ lVal sovrascrivendo il valore originale:


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Passaggio [9. Disconnettere la pagina delle proprietà](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



