---
title: Metodi facoltativi
description: Metodi facoltativi
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118491"
---
# <a name="optional-methods"></a>Metodi facoltativi

Un componente OLE può implementare un'interfaccia senza implementare tutta la semantica di ogni metodo nell'interfaccia, restituendo invece E \_ NOTIMPL o S \_ OK in base alle esigenze. Nella tabella seguente vengono descritti i metodi che non devono essere implementati da un contenitore di controlli ActiveX (ovvero il contenitore di controlli può restituire E \_ NOTIMPL).

La tabella seguente descrive i metodi facoltativi. Si noti che il metodo deve ancora esistere, ma può semplicemente restituire E \_ NOTIMPL anziché implementare la semantica reale. Si noti che tutti i metodi di un'interfaccia obbligatoria non elencati di seguito devono essere considerati obbligatori e non possono restituire E \_ NOTIMPL.

## <a name="ioleclientsite"></a>IOleClientSite



| Metodo                                                     | Commenti                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**SaveObject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Necessaria per il corretto supporto della persistenza.<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Necessaria solo se il contenitore supporta il collegamento a controlli all'interno di un modulo o di un documento.<br/> |



 

## <a name="ioleinplacesite"></a>IOleInPlaceSite



| Metodo                                                                     | Commenti                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Facoltativo<br/>                                      |
| [**Scorrimento**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Può restituire S \_ false senza azione.<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Può restituire S \_ OK senza alcuna azione.<br/>              |
| [**DeactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | La disattivazione è obbligatoria. Undo è facoltativo. <br/> |



 

## <a name="iolecontrolsite"></a>IOleControlSite



| Metodo                                                                          | Commenti                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Necessaria per i contenitori che supportano i controlli estesi.<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Necessaria per i contenitori che desiderano includere le proprie pagine delle proprietà per gestire le proprietà di controllo estese, oltre a quelle fornite da un controllo.<br/> |
| [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Può restituire S \_ false senza azione.<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Facoltativo<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (proprietà di ambiente)



| Metodo                      | Commenti                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Necessaria per i contenitori che supportano le proprietà di ambiente non standard.<br/> |
| GetTypeInfo<br/>      | Necessaria per i contenitori che supportano le proprietà di ambiente non standard.<br/> |
| GetIDsOfNames<br/>    | Necessaria per i contenitori che supportano le proprietà di ambiente non standard.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (sink di evento)



| Metodo                      | Commenti                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Il controllo è in grado di riconoscere le proprie informazioni sul tipo, pertanto non è necessario chiamarlo.<br/> |
| GetTypeInfo<br/>      | Il controllo è in grado di riconoscere le proprie informazioni sul tipo, pertanto non è necessario chiamarlo.<br/> |
| GetIDsOfNames<br/>    | Il controllo è in grado di riconoscere le proprie informazioni sul tipo, pertanto non è necessario chiamarlo.<br/> |



 

## <a name="ioleinplaceframe"></a>IOleInPlaceFrame



| Metodo                                                                           | Commenti                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Necessaria per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Necessaria per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Necessaria per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)<br/> |
| [**InsertMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Necessaria per i contenitori con interfaccia utente di menu (facoltativo)<br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Necessaria per i contenitori con interfaccia utente di menu (facoltativo)<br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Necessaria per i contenitori con interfaccia utente di menu (facoltativo)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Necessaria solo per i contenitori con una riga di stato<br/>        |
| [**EnableModeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Facoltativo<br/>                                                     |
| [**TranslateAccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Facoltativo<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| Metodo                                                                    | Commenti                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ParseDisplayName**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | Solo se è supportato il collegamento a controlli o altri incorporamenti nel contenitore, perché questa operazione è necessaria per l'associazione del moniker.<br/>                                                                                                                  |
| [**LockContainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | Come per ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Restituisce tutti i controlli ActiveX tramite un enumeratore con [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), ma non necessariamente tutti gli oggetti (poiché non c'è alcuna garanzia che tutti gli oggetti siano controlli ActiveX; alcuni possono essere controlli di Windows normali).<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

