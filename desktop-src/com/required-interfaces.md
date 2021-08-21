---
title: Interfacce obbligatorie (COM)
description: Informazioni sulle interfacce ActiveX contenitori di controllo che possono o devono essere implementate dai contenitori di controlli.
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf19cb8d0c72b365f6a8faa263fc76ddede1e5231fc34a9090c064f54d75b7f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309663"
---
# <a name="required-interfaces-com"></a>Interfacce obbligatorie (COM)

La tabella seguente elenca le interfacce ActiveX Contenitore di controllo e indica quali interfacce sono facoltative e quali sono obbligatorie e devono essere implementate dai contenitori di controllo.



| Interfaccia                                                                      | Necessaria?      | Commenti                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ioleclientsite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Sì<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**Iadvisesink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | No<br/>  | Solo quando il contenitore desidera (a) notifiche di modifica dei dati (controlli con [**IDataObject),**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)(b) notifica di modifica della visualizzazione (controlli che non sono attivi e hanno [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) o [**IViewObject2)**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)e (c) altre notifiche dai controlli che agiscono come oggetti incorporati standard.<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Sì<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Sì<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**Ioleinplaceframe**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Sì<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Sì<br/> | Vedere la nota 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch** per le proprietà di ambiente<br/>                                | Sì<br/> | Vedere la nota 2 e [Le proprietà di ambiente per i controlli](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Set di eventi di controllo<br/>                                                  | Sì<br/> | Vedere la nota 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | No<br/>  | [**ISimpleFrameSite e**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) il supporto per i frame semplici annidati sono facoltativi.<br/>                                                                                                                                                                                                                                                    |
| [Ipropertynotifysink](data-binding-through-ipropertynotifysink.md)<br/> | No<br/>  | Necessario solo per i contenitori che (a) hanno una propria interfaccia utente di modifica delle proprietà che richiede l'aggiornamento ogni volta che un controllo modifica una proprietà o (b) vuole controllare le modifiche delle proprietà requestedit e altre funzionalità di data binding di questo \[ [](/windows/desktop/Midl/requestedit) \] tipo.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Sì<br/> | Obbligatorio se il contenitore supporta interfacce duali. Vedere la nota 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | No<br/>  | Il supporto è fortemente consigliato.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer viene**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) implementato nell'oggetto documento o modulo (o analogo appropriato) che contiene i siti contenitore. I controlli **usano IOleContainer** per passare ad altri controlli nello stesso documento o modulo.
2.  Il supporto per le interfacce duali non è obbligatorio, ma è fortemente consigliato. La ActiveX contenitori di controlli per sfruttare i vantaggi delle interfacce duali offrirà prestazioni migliori con i controlli che offrono supporto per la doppia interfaccia.

ActiveX contenitori di controlli devono supportare le eccezioni di automazione OLE. Se un contenitore di controlli supporta interfacce duali, deve acquisire le eccezioni di automazione tramite [IErrorInfo.](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

