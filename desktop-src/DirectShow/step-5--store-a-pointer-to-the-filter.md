---
description: Passaggio 5.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Passaggio 5. Archiviare un puntatore al filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232985"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Passaggio 5. Archiviare un puntatore al filtro

Eseguire l'override del metodo [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) per archiviare un puntatore al filtro. Nell'esempio seguente viene eseguita una query sul parametro *punk* per l'interfaccia ISaturation personalizzata del filtro:


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



[Passaggio 6: Inizializzare la finestra di dialogo](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



