---
title: Uso dell'annotazione diretta
description: Uso dell'annotazione diretta
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8543b5aa4e6beb86b6119d13fe71ad45c1a34776e19095170cb48d8d9f48e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744886"
---
# <a name="using-direct-annotation"></a>Uso dell'annotazione diretta

**Per usare l'annotazione diretta per eseguire l'override del valore di una proprietà**

1.  Usare la [funzione CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) per creare [**l'oggetto IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
2.  Chiamare [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passando **HWND,** ID oggetto, ID figlio, proprietà da sottoporre a override e [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) contenente il nuovo valore della proprietà. Questo passaggio annota il valore.
3.  Rilasciare i puntatori a interfaccia e liberare memoria.

Nell'esempio seguente viene illustrato come annotare la [**proprietà Role**](role-property.md) di un controllo testo statico.


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

Le proprietà Microsoft Active Accessibility seguenti possono essere annotate quando si specifica un valore (dove il valore deve essere del tipo annotato) per l'annotazione diretta. Per eseguire l'override o aggiungere una proprietà di Microsoft Automazione interfaccia utente a un controllo, è possibile specificare l'ID della proprietà Automazione interfaccia utente anziché l'ID Microsoft Active Accessibility proprietà. Per un elenco di ID Automazione interfaccia utente, vedere [Identificatori di proprietà.](uiauto-entry-propids.md)



| Proprietà                      | Type     |
|-------------------------------|----------|
| NOME ACC \_ \_ PROPID             | VT \_ BSTR |
| DESCRIZIONE DI PROPID \_ ACC \_      | VT \_ BSTR |
| RUOLO DI ACCESSO \_ \_ PROPID             | VT \_ I4   |
| STATO DI \_ ACC \_ PROPID            | VT \_ I4   |
| GUIDA DI PROPID \_ ACC \_             | VT \_ BSTR |
| PROPID \_ ACC \_ KEYBOARDSHORTCUT | VT \_ BSTR |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR |
| VALUEMAP \_ DI PROPID ACC \_         | VT \_ BSTR |
| PROPID \_ ACC \_ ROLEMAP          | VT \_ BSTR |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR |



 

 

 