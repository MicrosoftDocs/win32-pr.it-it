---
description: Implementare l'interfaccia ISpecifyPropertyPages nel filtro come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: 'Passaggio 2: Implementare ISpecifyPropertyPages'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe37a22c6ba9c14f8656ac41294360569316be1a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410054"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Passaggio 2: Implementare ISpecifyPropertyPages

Implementare quindi **l'interfaccia ISpecifyPropertyPages** nel filtro. Questa interfaccia ha un singolo metodo, **GetPages,** che restituisce una matrice di CLSID per le pagine delle proprietà supportate dal filtro. In questo esempio il filtro ha una singola pagina delle proprietà. Per iniziare, generare il CLSID e dichiararlo nel file di intestazione:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Implementare ora **il metodo GetPages:**


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



Allocare memoria per la matrice usando **CoTaskMemAlloc.** Il chiamante rilascerà la memoria.

Passaggio [successivo: Passaggio 3. Supporto di QueryInterface.](step-3--support-queryinterface.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



