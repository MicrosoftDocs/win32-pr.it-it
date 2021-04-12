---
title: Uso dell'annotazione diretta
description: Uso dell'annotazione diretta
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338175"
---
# <a name="using-direct-annotation"></a>Uso dell'annotazione diretta

**Per utilizzare l'annotazione diretta per eseguire l'override del valore di una proprietà**

1.  Utilizzare la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) per creare l'oggetto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
2.  Chiamare [**IAccPropServices:: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passando **HWND**, ID oggetto, ID figlio, la proprietà di cui eseguire l'override e una [variante](/windows/win32/api/oaidl/ns-oaidl-variant) che contiene il nuovo valore della proprietà. Questo passaggio annota il valore.
3.  Rilasciare i puntatori all'interfaccia e liberare la memoria.

Nell'esempio seguente viene illustrato come annotare la proprietà [**Role**](role-property.md) di un controllo testo statico.


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a>Proprietà supportate quando si specifica un valore

Le seguenti proprietà di Microsoft Active Accessibility possono essere annotate quando si specifica un valore (il cui valore deve essere del tipo indicato) per l'annotazione diretta. Per eseguire l'override o aggiungere una proprietà di automazione interfaccia utente Microsoft a un controllo, è possibile specificare l'ID della proprietà di automazione interfaccia utente anziché l'ID della proprietà Microsoft Active Accessibility. Per un elenco di ID di automazione interfaccia utente, vedere [identificatori di proprietà](uiauto-entry-propids.md).



| Proprietà                      | Type     |
|-------------------------------|----------|
| \_nome ACC \_ propid             | \_BSTR VT |
| \_Descrizione ACC \_ propid      | \_BSTR VT |
| \_ruolo ACC \_ propid             | VT \_ I4   |
| \_stato ACC \_ propid            | VT \_ I4   |
| Guida di PROPID \_ ACC \_             | \_BSTR VT |
| \_KEYBOARDSHORTCUT ACC \_ propid | \_BSTR VT |
| \_DefaultAction propid ACC \_    | \_BSTR VT |
| \_VALUEMAP ACC \_ propid         | \_BSTR VT |
| \_ROLEMAP ACC \_ propid          | \_BSTR VT |
| \_STATEMAP ACC \_ propid         | \_BSTR VT |



 

 

 