---
title: Utilizzo di IADsExtension
description: Questo argomento contiene esempi di codice C++ per l'uso dell'interfaccia IADsExtension.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a844d320b28548e9e9998881fd2a09815d1882e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220913"
---
# <a name="iadsextension-usage"></a>Utilizzo di IADsExtension

[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) è un'interfaccia facoltativa implementata dal writer di estensione quando viene soddisfatta almeno una delle condizioni seguenti:

-   Il componente di estensione richiede una notifica di inizializzazione come definito da **ADSI \_ ext \_ * dwCode*** nel metodo [**opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .
-   L'estensione supporta un'interfaccia duale o dispatch.

Se un componente di estensione supporta l'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per il primo motivo, i metodi [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**IADsExtension::P rivateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) possono restituire **E \_ NOTIMPL**. In alternativa, se un componente di estensione supporta un'interfaccia duale o dispatch, il metodo [**opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) può ignorare i dati e restituire un valore **HRESULT** di **e \_ NOTIMPL**.

Nel codice seguente viene illustrata un'estensione che implementa [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).


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



 

 




