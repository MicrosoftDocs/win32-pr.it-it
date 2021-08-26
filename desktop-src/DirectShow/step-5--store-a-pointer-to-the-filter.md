---
description: Archiviare un puntatore a un filtro come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Passaggio 5. Archiviare un puntatore al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63becf4cb98f401a4810f0f9a2604ef65387a58d08d84b9f670c09b51fe9acd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078771"
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

 

 



