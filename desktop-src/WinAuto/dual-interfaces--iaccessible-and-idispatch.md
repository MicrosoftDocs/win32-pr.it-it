---
title: Interfacce duali IAccessible e IDispatch
description: Gli sviluppatori di server devono fornire il IDispatch dell'interfaccia standard Component Object Model (COM) per i relativi oggetti accessibili.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299840"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a>Interfacce doppie: IAccessible e IDispatch

Gli sviluppatori di server devono fornire il [**IDispatch**](idispatch-interface.md) dell'interfaccia standard Component Object Model (com) per i relativi oggetti accessibili. L'interfaccia IDispatch consente alle applicazioni client scritte in Microsoft Visual Basic e a diversi linguaggi di scripting di utilizzare i metodi e le proprietà esposti da [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Poiché un oggetto accessibile fornisce l'accesso a un oggetto indirettamente tramite [IDispatch:: Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) o direttamente con **IAccessible**, si dice che dispone di un'interfaccia duale.

Quando i client C/C++ ottengono un puntatore di interfaccia IDispatch, i client possono chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per provare a convertire il puntatore dell'interfaccia IDispatch in un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Per chiamare indirettamente i metodi **IAccessible** , i client C/C++ chiamano IDispatch:: Invoke. Per migliorare le prestazioni, chiamare i metodi **IAccessible** per utilizzare l'oggetto direttamente.

Per un elenco degli ID di invio (DISPID) usati da **IDispatch** per identificare i metodi e le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , vedere [Appendice C: IAccessible DISPID](appendix-c--iaccessible-dispids.md).

> [!Note]  
> Nella versione 2,0 e successive di Microsoft Active Accessibility, i server non devono implementare completamente i metodi di [**IDispatch**](idispatch-interface.md) ma possono semplicemente restituire E \_ NOTIMPL dopo l'inizializzazione di tutti i parametri out, come illustrato nell'esempio seguente.

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 