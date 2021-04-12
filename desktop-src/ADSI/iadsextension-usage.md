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
# <a name="iadsextension-usage"></a><span data-ttu-id="09bd1-104">Utilizzo di IADsExtension</span><span class="sxs-lookup"><span data-stu-id="09bd1-104">IADsExtension Usage</span></span>

<span data-ttu-id="09bd1-105">[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) è un'interfaccia facoltativa implementata dal writer di estensione quando viene soddisfatta almeno una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="09bd1-105">[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) is an optional interface implemented by the extension writer when at least one of the following conditions are met:</span></span>

-   <span data-ttu-id="09bd1-106">Il componente di estensione richiede una notifica di inizializzazione come definito da **ADSI \_ ext \_ \* dwCode**\* nel metodo [**opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .</span><span class="sxs-lookup"><span data-stu-id="09bd1-106">The extension component requires an initialization notification as defined by **ADSI\_EXT\_\*dwCode**\* in the [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span>
-   <span data-ttu-id="09bd1-107">L'estensione supporta un'interfaccia duale o dispatch.</span><span class="sxs-lookup"><span data-stu-id="09bd1-107">The extension supports a dual or dispatch interface.</span></span>

<span data-ttu-id="09bd1-108">Se un componente di estensione supporta l'interfaccia [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) per il primo motivo, i metodi [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**IADsExtension::P rivateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) possono restituire **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="09bd1-108">If an extension component supports the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for the first reason, the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**IADsExtension::PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods can return **E\_NOTIMPL**.</span></span> <span data-ttu-id="09bd1-109">In alternativa, se un componente di estensione supporta un'interfaccia duale o dispatch, il metodo [**opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) può ignorare i dati e restituire un valore **HRESULT** di **e \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="09bd1-109">Alternatively, if an extension component supports a dual or dispatch interface , the [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method can ignore the data and return an **HRESULT** of **E\_NOTIMPL**.</span></span>

<span data-ttu-id="09bd1-110">Nel codice seguente viene illustrata un'estensione che implementa [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="09bd1-110">The following code shows an extension implementing [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>


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



 

 




