---
title: Metodi facoltativi nelle interfacce di controllo
description: Metodi facoltativi nelle interfacce di controllo
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1409b1c8d22f85a48829c07155e03379fc79103c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955250"
---
# <a name="optional-methods-in-control-interfaces"></a>Metodi facoltativi nelle interfacce di controllo

L'implementazione di un'interfaccia non implica necessariamente l'implementazione di tutti i metodi di tale interfaccia per eseguire operazioni più che restituire E \_ NOTIMPL o S OK, a seconda delle \_ esigenze. La tabella seguente identifica i metodi delle interfacce elencate nell'argomento [supporto di un'interfaccia](what-support-for-an-interface-means.md) che può essere implementato da un controllo in questo modo. Tutti i metodi non elencati devono essere implementati completamente se l'interfaccia è supportata.



| IOleControl                                                                                                   | Commenti                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **onmnemonico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obbligatorio per i controlli con i tasti di scelta.<br/>                              |
| [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obbligatorio per i controlli che utilizzano le proprietà di ambiente.<br/>                 |
| [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Vedi [blocco eventi](event-freezing.md)<br/>                            |
| IOleObject                                                                                                    |                                                                                |
| [**SetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obbligatorio se il controllo non è contrassegnato con OLEMISC \_ CANTLINKINSIDE<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obbligatorio se il controllo non è contrassegnato con OLEMISC \_ CANTLINKINSIDE<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Facoltativo<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Facoltativo<br/>                                                            |
| [**SetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Obbligatorio solo per il \_ contenuto di DVASPECT<br/>                                |
| [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Obbligatorio solo per il \_ contenuto di DVASPECT<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Facoltativo<br/>                                                            |
| [**DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Vedere la nota 1<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Facoltativo<br/>                                                            |
| [**ReactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Facoltativo<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Facoltativo<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Freeze**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Facoltativo<br/>                                                            |
| [**Sblocca**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Facoltativo<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Facoltativo<br/>                                                            |
| IPersistStream, IPersistStreamInit, Metodo IPersistMemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Vedere la nota 2<br/>                                                          |



 

1.  Un controllo con le pagine delle proprietà deve supportare [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) per le \_ Proprietà OLEIVERB e i \_ verbi primari OLEIVERB. Un controllo che può essere attivo deve supportare **DoVerb** per il \_ verbo INPLACEACTIVATE di OLEIVERB. Un controllo che può essere attivo dall'interfaccia utente deve supportare anche **DoVerb** per il \_ verbo UIACTIVATE di OLEIVERB.
2.  Se un controllo supporta [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) e può restituire un valore accurato, è consigliabile eseguire questa operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

 





