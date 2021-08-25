---
title: Metodi facoltativi nelle interfacce di controllo
description: Metodi facoltativi nelle interfacce di controllo
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92303b9e4e6a5edd295d0895a9121eee70ea05ae2a8967a9346ea26b153e8b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859291"
---
# <a name="optional-methods-in-control-interfaces"></a>Metodi facoltativi nelle interfacce di controllo

L'implementazione di un'interfaccia non significa necessariamente implementare tutti i metodi di tale interfaccia per eseguire altre attività oltre a restituire E NOTIMPL o \_ S OK in base alle \_ esigenze. Nella tabella seguente vengono identificati i metodi [](what-support-for-an-interface-means.md) delle interfacce elencati nell'argomento Informazioni sul supporto per un'interfaccia che un controllo può implementare in questo modo. Qualsiasi metodo non elencato qui deve essere completamente implementato se l'interfaccia è supportata.



| IOleControl                                                                                                   | Commenti                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obbligatorio per i controlli con mnemonici.<br/>                              |
| [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obbligatorio per i controlli che usano proprietà di ambiente.<br/>                 |
| [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Vedere Blocco [degli eventi](event-freezing.md)<br/>                            |
| Ioleobject                                                                                                    |                                                                                |
| [**SetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obbligatorio se il controllo non è contrassegnato con OLEMISC \_ CANTLINKINSIDE<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obbligatorio se il controllo non è contrassegnato con OLEMISC \_ CANTLINKINSIDE<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Facoltativo<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Facoltativo<br/>                                                            |
| [**SetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Obbligatorio solo per DVASPECT \_ CONTENT<br/>                                |
| [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Obbligatorio solo per DVASPECT \_ CONTENT<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Facoltativo<br/>                                                            |
| [**Doverb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Vedere la nota 1<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Facoltativo<br/>                                                            |
| [**RiattivazioneAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Facoltativo<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Facoltativo<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Freeze**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Facoltativo<br/>                                                            |
| [**Sbloccare**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Facoltativo<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Facoltativo<br/>                                                            |
| IPersistStream, IPersistStreamInit, IPersistMemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Vedere la nota 2<br/>                                                          |



 

1.  Un controllo con pagine delle proprietà deve supportare [**IOleObject::D oVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) per i verbi OLEIVERB PROPERTIES e \_ OLEIVERB \_ PRIMARY. Un controllo che può essere attivo deve supportare **DoVerb** per il verbo OLEIVERB \_ INPLACEACTIVATE. Un controllo che può essere attivo dell'interfaccia utente deve supportare **anche DoVerb** per il verbo OLEIVERB \_ UIACTIVATE.
2.  Se un controllo supporta [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) e può restituire un valore accurato, è consigliabile farlo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

 





