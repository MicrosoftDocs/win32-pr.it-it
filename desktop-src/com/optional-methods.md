---
title: Metodi facoltativi
description: Metodi facoltativi
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d64f4b22693c77295d3a21cfb59055f9a232d08bb1426d995f710bbf24073d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130043"
---
# <a name="optional-methods"></a>Metodi facoltativi

Un componente OLE può implementare un'interfaccia senza implementare tutta la semantica di ogni metodo nell'interfaccia, ma restituire E NOTIMPL o S OK in \_ \_ base alle esigenze. La tabella seguente descrive i metodi che un contenitore di ActiveX non deve implementare,ad esempio il contenitore di controlli può restituire E \_ NOTIMPL.

La tabella seguente descrive i metodi facoltativi. Si noti che il metodo deve ancora esistere, ma può semplicemente restituire E \_ NOTIMPL anziché implementare una semantica reale. Si noti che qualsiasi metodo di un'interfaccia obbligatoria non elencata di seguito deve essere considerato obbligatorio e non può restituire E \_ NOTIMPL.

## <a name="ioleclientsite"></a>Ioleclientsite



| Metodo                                                     | Commenti                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**SaveObject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Necessario per il corretto supporto della persistenza.<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Necessario solo se il contenitore supporta il collegamento ai controlli all'interno del proprio modulo o documento.<br/> |



 

## <a name="ioleinplacesite"></a>IOleInPlaceSite



| Metodo                                                                     | Commenti                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Facoltativo<br/>                                      |
| [**Scorrimento**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Può restituire S \_ FALSE senza alcuna azione.<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Può restituire S \_ OK senza alcuna azione.<br/>              |
| [**DeactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | La disattivazione è obbligatoria. L'annullamento è facoltativo. <br/> |



 

## <a name="iolecontrolsite"></a>IOleControlSite



| Metodo                                                                          | Commenti                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Necessario per i contenitori che supportano i controlli estesi.<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Necessario per i contenitori che desiderano includere le proprie pagine delle proprietà per gestire le proprietà estese del controllo oltre a quelle fornite da un controllo .<br/> |
| [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Può restituire S \_ FALSE senza alcuna azione.<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Facoltativo<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (proprietà di ambiente)



| Metodo                      | Commenti                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Necessario per i contenitori che supportano proprietà di ambiente non standard.<br/> |
| GetTypeInfo<br/>      | Necessario per i contenitori che supportano proprietà di ambiente non standard.<br/> |
| Getidsofnames<br/>    | Necessario per i contenitori che supportano proprietà di ambiente non standard.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (sink di evento)



| Metodo                      | Commenti                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Il controllo conosce le proprie informazioni sul tipo, quindi non è necessario chiamarlo.<br/> |
| GetTypeInfo<br/>      | Il controllo conosce le proprie informazioni sul tipo, quindi non è necessario chiamarlo.<br/> |
| Getidsofnames<br/>    | Il controllo conosce le proprie informazioni sul tipo, quindi non è necessario chiamarlo.<br/> |



 

## <a name="ioleinplaceframe"></a>Ioleinplaceframe



| Metodo                                                                           | Commenti                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Necessario per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Necessario per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Necessario per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)<br/> |
| [**InsertMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Necessario per i contenitori con interfaccia utente del menu (facoltativo)<br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Necessario per i contenitori con interfaccia utente del menu (facoltativo)<br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Necessario per i contenitori con interfaccia utente del menu (facoltativo)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Necessario solo per i contenitori con una riga di stato<br/>        |
| [**EnableModeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Facoltativo<br/>                                                     |
| [**TranslateAccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Facoltativo<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| Metodo                                                                    | Commenti                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ParseDisplayName**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | È supportato solo il collegamento a controlli o ad altri incorporamenti nel contenitore, in quanto ciò è necessario per l'associazione di moniker.<br/>                                                                                                                  |
| [**LockContainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | Come per ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Restituisce tutti i controlli ActiveX tramite un [**enumeratore con IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), ma non necessariamente tutti gli oggetti (perché non c'è alcuna garanzia che tutti gli oggetti siano ActiveX controlli; alcuni possono essere controlli Windows controllo).<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

