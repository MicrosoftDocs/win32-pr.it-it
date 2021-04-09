---
title: Interfaccia IADsExtension
description: Questo argomento contiene esempi di codice C++ per l'uso dell'interfaccia IADsExtension.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- IADsExtension ADSI, utilizzo
- ADSI ADSI, codice di esempio C/C++, uso di IADsExtension
- estensioni ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c950b6d305cc4c90ed75ff0cc96b5f7f344e12
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730226"
---
# <a name="iadsextension-interface"></a>Interfaccia IADsExtension

L'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) è definita come segue:


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



Aggregator (ADSI) chiama il metodo [**IADsExtension:: opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) . L'estensione deve interpretare il parametro *dwCode* e ogni parametro *vardata* , in base alla documentazione del provider.

Aggregator (ADSI), chiama il metodo [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . Viene chiamato dopo che ADSI determina l'estensione per la distribuzione del servizio. L'estensione può usare le informazioni sul tipo per ottenere il DISPID, ovvero usando la funzione [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .

ADSI chiama in genere il metodo [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) dopo aver chiamato la funzione [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . L'estensione deve chiamare il metodo effettivo che implementa. In alternativa, l'estensione può usare le informazioni sul tipo e chiamare la funzione [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .

Tutti i parametri hanno lo stesso significato dei parametri nel metodo [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) standard.

 

 