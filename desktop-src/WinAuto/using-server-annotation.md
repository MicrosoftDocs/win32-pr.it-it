---
title: Uso dell'annotazione server
description: In questo argomento vengono fornite informazioni sull'utilizzo delle annotazioni server per specificare un oggetto callback.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb545cd4dd016901d69f67d5ab5cab15dda08875
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300033"
---
# <a name="using-server-annotation"></a>Uso dell'annotazione server

In questo argomento vengono fornite informazioni sull'utilizzo delle annotazioni server per specificare un oggetto callback.

**Per eseguire l'override di una proprietà che specifica un oggetto callback**

1.  Ottenere un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) all'elemento accessibile da annotare.
2.  Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'elemento accessible per ottenere un puntatore di interfaccia [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .
3.  Chiamare [**IAccIdentity:: GetIdentityString ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) sul puntatore a interfaccia [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) per ottenere una stringa che identifichi in modo univoco l'elemento accessibile da annotare.
4.  Utilizzare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) per creare l'oggetto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
5.  Creare un oggetto Component Object Model (COM) che implementi [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver).
6.  Chiamare [**IAccPropServices:: SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver), passando la stringa di identità, un GUID che indica la proprietà di cui eseguire l'override e un puntatore all'oggetto callback [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) .
7.  Puntatori dell'interfaccia di versione e memoria libera.

Quando un client richiede la proprietà dell'elemento accessible, viene chiamato l'oggetto callback e il valore viene restituito al client.

Come quando si specifica un valore, gli sviluppatori di server possono usare in alternativa il metodo [**IAccPropServices:: ComposeHwndIdentityString**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) per ottenere una stringa di identità. in alternativa, è possibile usare il metodo [**IAccPropServices:: SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) e specificare i parametri *HWND*, *idObject* o *idChild* anziché una stringa di identità.

Quando si utilizza [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) o [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) su un oggetto contenitore, gli sviluppatori di server possono facoltativamente specificare che anche le informazioni di override devono essere applicate a tutti gli elementi figlio di tale contenitore.

I server possono cancellare in modo esplicito l'annotazione in qualsiasi momento usando [**IAccPropServices:: ClearProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops). Questa operazione non è in genere necessaria perché il servizio di annotazione pulisce automaticamente e rilascia le informazioni di annotazione quando l'elemento accessibile annotato scompare.

Di seguito è riportato un elenco di proprietà che possono essere annotate mediante questa procedura.

## <a name="properties-supported-when-specifying-a-callback"></a>Proprietà supportate quando si specifica un callback

Quando si specifica un callback, è possibile annotare le proprietà seguenti. Attualmente queste proprietà non possono essere annotate direttamente specificando un valore.



| Proprietà                      | Type                                                             |
|-------------------------------|------------------------------------------------------------------|
| \_nome ACC \_ propid             | \_BSTR VT                                                         |
| \_Descrizione ACC \_ propid      | \_BSTR VT                                                         |
| \_ruolo ACC \_ propid             | VT \_ I4                                                           |
| \_stato ACC \_ propid            | VT \_ I4                                                           |
| Guida di PROPID \_ ACC \_             | \_BSTR VT                                                         |
| \_KEYBOARDSHORTCUT ACC \_ propid | \_BSTR VT                                                         |
| \_DefaultAction propid ACC \_    | \_BSTR VT                                                         |
| \_VALUEMAP ACC \_ propid         | \_BSTR VT                                                         |
| \_ROLEMAP ACC \_ propid          | \_BSTR VT                                                         |
| \_STATEMAP ACC \_ propid         | \_BSTR VT                                                         |
| \_ \_ stato attivo ACC propid            | \_invio VT<br/> VT \_ I4<br/>                        |
| \_selezione ACC \_ propid        | \_invio VT<br/> VT \_ I4<br/> VT \_ sconosciuto<br/> |
| \_padre ACC \_ propid           | \_invio VT                                                     |
| PROPID \_ di \_ navigazione \_ ACC          | \_invio VT<br/> VT \_ I4<br/>                        |
| PROPID \_ di \_ navigazione ACC \_ giù        | \_invio VT<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV a \_ sinistra        | \_invio VT<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV a \_ destra       | \_invio VT<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ precedente        | \_invio VT<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ Avanti        | \_invio VT<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ FIRSTCHILD  | \_invio VT<br/> VT \_ I4<br/>                        |
| PROPID \_ ACC \_ NAV \_ LastChild   | \_invio VT<br/> VT \_ I4<br/>                        |



 

 

