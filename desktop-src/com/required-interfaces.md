---
title: Interfacce obbligatorie (COM)
description: Interfacce obbligatorie
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df483f8c8aa5eb5ecb6799b834fccab42f42ca1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300806"
---
# <a name="required-interfaces-com"></a>Interfacce obbligatorie (COM)

La tabella seguente elenca le interfacce del contenitore di controlli ActiveX e indica quali interfacce sono facoltative e quali sono obbligatorie e devono essere implementate dai contenitori di controlli.



| Interfaccia                                                                      | Necessaria?      | Commenti                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Sì<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | No<br/>  | Solo quando il contenitore desidera (a) notifiche di modifica dei dati (controlli con [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)), (b) visualizzazione della notifica di modifica (controlli che non sono attivi e con [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) o [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)) e (c) altre notifiche da controlli che fungono da oggetti incorporati standard.<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Sì<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Sì<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Sì<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Sì<br/> | Vedere la nota 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch** per le proprietà di ambiente<br/>                                | Sì<br/> | Vedere la nota 2 e le [proprietà di ambiente per i controlli](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Controllare i set di eventi<br/>                                                  | Sì<br/> | Vedere la nota 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | No<br/>  | [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e il supporto per i frame semplici annidati sono facoltativi.<br/>                                                                                                                                                                                                                                                    |
| [IPropertyNotifySink](data-binding-through-ipropertynotifysink.md)<br/> | No<br/>  | Necessaria solo per i contenitori che (a) hanno una propria interfaccia utente per la modifica delle proprietà che richiederebbe l'aggiornamento ogni volta che un controllo modifica una proprietà o (b) desidera controllare \[ [](/windows/desktop/Midl/requestedit) \] le modifiche delle proprietà requestedit e altre funzionalità di data binding.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Sì<br/> | Obbligatorio se il contenitore supporta le interfacce duali. Vedere la nota 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | No<br/>  | Il supporto è fortemente consigliato.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) viene implementato nel documento o nell'oggetto Form (o analogo appropriato) che include i siti del contenitore. I controlli usano **IOleContainer** per passare ad altri controlli nello stesso documento o modulo.
2.  Il supporto per le interfacce duali non è obbligatorio, ma è fortemente consigliato. La scrittura di contenitori di controlli ActiveX per sfruttare le interfacce duali offrirà prestazioni migliori con i controlli che offrono il supporto dell'interfaccia duale.

I contenitori di controlli ActiveX devono supportare le eccezioni di automazione OLE. Se un contenitore di controlli supporta le interfacce duali, deve acquisire le eccezioni di automazione tramite [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

