---
title: Uso dell'annotazione server
description: In questo argomento vengono fornite informazioni sull'uso dell'annotazione server per specificare un oggetto callback.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b2955d49431b502c8587484208321bc1ab1bc0c8201fabf466b60b68f548a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823905"
---
# <a name="using-server-annotation"></a>Uso dell'annotazione server

In questo argomento vengono fornite informazioni sull'uso dell'annotazione server per specificare un oggetto callback.

**Per eseguire l'override di una proprietà che specifica un oggetto callback**

1.  Ottenere un [**puntatore a interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) all'elemento accessibile da annotare.
2.  Chiamare [**QueryInterface sull'elemento**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) accessibile per ottenere un puntatore a interfaccia [**IAccIdentity.**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity)
3.  Chiamare [**IAccIdentity::GetIdentityString()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) sul puntatore a interfaccia [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) per ottenere una stringa che identifica in modo univoco l'elemento accessibile da annotare.
4.  Usare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) per creare [**l'oggetto IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
5.  Creare un Component Object Model (COM) che implementa [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver).
6.  Chiamare [**IAccPropServices::SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver), passando la stringa di identità, un GUID che indica la proprietà da sottoporre a override e un puntatore all'oggetto callback [**IAccPropServer.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)
7.  Rilasciare puntatori a interfaccia e liberare memoria.

Quando un client richiede la proprietà dell'elemento accessibile, l'oggetto callback verrà chiamato e restituirà il valore al client.

Come quando si specifica un valore, gli sviluppatori di server possono in alternativa usare il metodo [**IAccPropServices::ComposeHwndIdentityString**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) per ottenere una stringa di identità. oppure possono usare il [**metodo IAccPropServices::SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) e specificare i parametri *hwnd*, *idObject* o *idChild* anziché una stringa di identità.

Quando si usa [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) o [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) in un oggetto contenitore, gli sviluppatori del server possono specificare facoltativamente che le informazioni di override devono essere applicate anche a tutti gli elementi figlio del contenitore.

I server possono cancellare in modo esplicito l'annotazione in qualsiasi momento usando [**IAccPropServices::ClearProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops). Questa operazione in genere non è necessaria, perché il servizio di annotazione pulirà e rilascerà automaticamente le informazioni sull'annotazione quando l'elemento accessibile annotato scompare.

Di seguito è riportato un elenco di proprietà che è possibile annotare usando questa procedura.

## <a name="properties-supported-when-specifying-a-callback"></a>Proprietà supportate quando si specifica un callback

Quando si specifica un callback, è possibile annotare le proprietà seguenti. Attualmente queste proprietà non possono essere annotate direttamente specificando un valore.



| Proprietà                      | Type                                                             |
|-------------------------------|------------------------------------------------------------------|
| NOME ACC \_ PROPID \_             | VT \_ BSTR                                                         |
| DESCRIZIONE DI PROPID \_ ACC \_      | VT \_ BSTR                                                         |
| RUOLO DI \_ ACCESSO \_ PROPID             | VT \_ I4                                                           |
| STATO \_ DI ACC \_ PROPID            | VT \_ I4                                                           |
| GUIDA DI PROPID \_ ACC \_             | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ KEYBOARDSHORTCUT | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ ROLEMAP          | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR                                                         |
| STATO ATTIVO DI PROPID \_ ACC \_            | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| SELEZIONE DI \_ PROPID ACC \_        | VT \_ DISPATCH<br/> VT \_ I4<br/> VT \_ UNKNOWN<br/> |
| PROPID \_ ACC \_ PARENT           | VT \_ DISPATCH                                                     |
| PROPID \_ ACC \_ NAV \_ UP          | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ DOWN        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC NAV A \_ \_ SINISTRA        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ RIGHT       | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ PREV        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ NEXT        | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ FIRSTCHILD  | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ LASTCHILD   | VT \_ DISPATCH<br/> VT \_ I4<br/>                        |



 

 

