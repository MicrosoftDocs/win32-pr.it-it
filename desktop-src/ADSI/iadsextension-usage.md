---
title: Utilizzo di IADsExtension
description: Questo argomento contiene esempi di codice C++ per l'uso dell'interfaccia IADsExtension.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- estensioni ADSI , IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbab6813a87701fe2d7e130a03540476412c9e13b9d5d3ca96bdd0e63b2dad54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023489"
---
# <a name="iadsextension-usage"></a>Utilizzo di IADsExtension

[**IADsExtension è**](/windows/desktop/api/Iads/nn-iads-iadsextension) un'interfaccia facoltativa implementata dal writer di estensioni quando viene soddisfatta almeno una delle condizioni seguenti:

-   Il componente di estensione richiede una notifica di inizializzazione come definito da **ADSI \_ EXT \_ *dwCode*** nel [**metodo Operate.**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate)
-   L'estensione supporta un'interfaccia duale o dispatch.

Se un componente di estensione supporta l'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per il primo motivo, i metodi [**IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**IADsExtension::P rivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) possono restituire **E \_ NOTIMPL.** In alternativa, se un componente di estensione supporta un'interfaccia duale o dispatch, il [**metodo Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) può ignorare i dati e restituire **un HRESULT** **di E \_ NOTIMPL.**

Il codice seguente illustra un'estensione che implementa [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).


```C++
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
    HRESULT hr = S_OK;
    switch (dwCode) 
    {
    case ADS_EXT_INIT:
         // Prompt for a credential.
         // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);
          break;
    default:
          hr = E_FAIL;
          break;
    }        
    return hr;        
}
 
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{        
      if (rgdispid == NULL)
      {
        return E_POINTER;
      }    
    return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
 
STDMETHOD(PrivateInvoke)(DISPID dispidMember, REFIID riid, LCID lcid, WORD wFlags, DISPPARAMS * pdispparams, VARIANT * pvarResult, EXCEPINFO * pexcepinfo, UINT * puArgErr)
{
 return DispInvoke( (IHelloWorld*)this, 
           m_pTypeInfo,
        dispidMember, 
        wFlags, 
        pdispparams, 
        pvarResult, 
        pexcepinfo, 
        puArgErr );
}
```



 

 




