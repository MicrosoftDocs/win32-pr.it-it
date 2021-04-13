---
description: Fornisce metodi che definiscono l'interazione tra un'interfaccia utente (UI) e gli oggetti dello spazio dei nomi di ricerca creati dall'indicizzatore.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Interfaccia ISearchItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401630"
---
# <a name="isearchitem-interface"></a>Interfaccia ISearchItem

Fornisce metodi che definiscono l'interazione tra un'interfaccia utente (UI) e gli oggetti dello spazio dei nomi di ricerca creati dall'indicizzatore.

## <a name="members"></a>Membri

L'interfaccia **ISearchItem** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISearchItem** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISearchItem** dispone di questi metodi.



| Metodo                                                         | Descrizione                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentFolder**](-search-isearchitem-getparentfolder.md) | Ottiene l'oggetto **ISearchItem** se l'URL rappresenta un'origine dati della shell effettiva, nota anche come estensione dello spazio dei nomi della shell.<br/> |
| [**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | Ottiene l'oggetto dell'interfaccia utente di **ISearchItem**.<br/>                                                                        |



 

## <a name="remarks"></a>Commenti

[**ISearchItem:: GetParentFolder**](-search-isearchitem-getparentfolder.md) è supportato solo in Windows XP e windows Server 2003 e non deve più essere utilizzato.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **ISearchItem** e le API seguenti: le interfacce [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
