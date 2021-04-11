---
title: Interfacce di documenti composti
description: Interfacce di documenti composti
ms.assetid: 3192ee58-55fd-43cb-b7d5-7270e91b8131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eecb44945ec666a38ebf59544caf2e09eb5930d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047419"
---
# <a name="compound-document-interfaces"></a>Interfacce di documenti composti

Nelle tabelle seguenti sono elencate le interfacce implementate da contenitori OLE, server OLE e oggetti documento composito. Le interfacce obbligatorie devono essere implementate sui componenti per i quali sono elencate. Tutte le altre funzionalità sono facoltative. Tuttavia, se si desidera includere una particolare funzionalità nell'applicazione, è necessario implementare le interfacce visualizzate per la funzionalità nella tabella seguente. Tutte le altre interfacce sono necessarie solo se si include una funzionalità specifica.

Nella tabella seguente sono elencati i comportamenti obbligatori e facoltativi per i contenitori OLE e le interfacce che è necessario implementare per ciascuna di esse.



| Comportamento                               | Interfacce                                                                                                                                                              |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comportamenti necessari<br/>          | [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/> [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                                                       |
| Filtro messaggi<br/>           | [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                                                     |
| Il collegamento<br/>                     | Nessuno<br/>                                                                                                                                                         |
| Collegamento a oggetti incorporati<br/> | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/> [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>             |
| Attivazione sul posto<br/>         | [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/> [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/> [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> |
| Trascinamento della selezione<br/>               | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                               |



 

Nella tabella seguente sono elencati i comportamenti obbligatori e facoltativi per i server OLE e i relativi oggetti documento compositi e le interfacce che è necessario implementare per ciascuna di esse. La tabella distingue i server OLE e i relativi oggetti per chiarire quale componente implementa le interfacce. La tabella nota anche i diversi requisiti degli oggetti forniti da out-of-process rispetto ai server in-process.



| Funzionalità                        | Server OLE                                                                                                                                | Oggetto (out-of-process)                                                                                                                         | Object (in-process)                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comportamenti necessari             | [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>                                                                                         | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)<br/> [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2)<br/> |
| Filtro messaggi<br/>   | [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                       |                                                                                                                                                 |                                                                                                                                                                                                                                             |
| Il collegamento<br/>             | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                 |                                                                                                                                                 | [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)<br/> [**IExternalConnection**](/windows/win32/api/objidlbase/nn-objidlbase-iexternalconnection)<br/>                                                                                                                                       |
| Attivazione sul posto<br/> |                                                                                                                                           | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                 | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                                                                                                             |
| Trascinamento della selezione<br/>       | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> |                                                                                                                                                 |                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

