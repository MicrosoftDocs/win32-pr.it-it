---
description: Definire un meccanismo per l'impostazione della proprietà come parte della creazione di una pagina delle proprietà del filtro per un filtro DirectShow personalizzato.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Passaggio 1. Definire un meccanismo per l'impostazione della proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410074"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>Passaggio 1. Definire un meccanismo per l'impostazione della proprietà

Il filtro deve supportare una modalità di comunicazione tra la pagina delle proprietà, in modo che la pagina delle proprietà possa impostare e recuperare le proprietà nel filtro. Di seguito sono riportati i possibili meccanismi:

-   Esporre un'interfaccia COM personalizzata.
-   Supporto delle proprietà di automazione tramite **IDispatch.**
-   Esporre **l'interfaccia IPropertyBag** e definire un set di proprietà denominate.

In questo esempio viene utilizzata un'interfaccia COM personalizzata, denominata ISaturation. Non si tratta di un'interfaccia DirectShow effettiva. è definito solo per questo esempio. Per iniziare, dichiarare l'interfaccia in un file di intestazione, insieme all'identificatore di interfaccia (IID):


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



È anche possibile definire l'interfaccia con IDL e usare il compilatore MIDL per creare il file di intestazione. Implementare quindi l'interfaccia personalizzata nel filtro. Questo esempio usa i metodi "Get" e "Set" per il valore di saturazione del filtro. Si noti che entrambi i metodi proteggono il membro \_ m lSaturation con una sezione critica.


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



Naturalmente, i dettagli della propria implementazione differiranno dall'esempio illustrato qui.

Passaggio [2. Implementare ISpecifyPropertyPages.](step-2--implement-ispecifypropertypages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



