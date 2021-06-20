---
description: Archiviare un puntatore a un filtro come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Passaggio 5. Archiviare un puntatore al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406794"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Passaggio 5. Archiviare un puntatore al filtro

Eseguire [**l'override del metodo CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) per archiviare un puntatore al filtro. L'esempio seguente esegue *una query sul parametro pUnk* per l'interfaccia ISaturation personalizzata del filtro:


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



Passaggio [successivo: Passaggio 6. Inizializzare la finestra di dialogo](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



