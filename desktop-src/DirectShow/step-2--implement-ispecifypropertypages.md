---
description: 'Passaggio 2:'
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: 'Passaggio 2: Implementare ISpecifyPropertyPages'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315532"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Passaggio 2: Implementare ISpecifyPropertyPages

Implementare quindi l'interfaccia **ISpecifyPropertyPages** nel filtro. Questa interfaccia dispone di un singolo metodo, **GetPages**, che restituisce una matrice di CLSID per le pagine delle proprietà supportate dal filtro. In questo esempio, il filtro ha una singola pagina delle proprietà. Per iniziare, generare il CLSID e dichiararlo nel file di intestazione:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Implementare ora il metodo **GetPages** :


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



Allocare memoria per la matrice utilizzando **CoTaskMemAlloc**. Il chiamante rilascerà la memoria.

Successivo: [passaggio 3. Supporta QueryInterface](step-3--support-queryinterface.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



