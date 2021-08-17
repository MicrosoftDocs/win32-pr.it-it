---
description: Fornisce metodi che definiscono l'interazione tra un'interfaccia utente e gli oggetti dello spazio dei nomi Search creati dall'indicizzatore.
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
ms.openlocfilehash: de3769f869838cd3a6660229a452ea7fbd96f943ac7421523c523662da205dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863954"
---
# <a name="isearchitem-interface"></a>Interfaccia ISearchItem

Fornisce metodi che definiscono l'interazione tra un'interfaccia utente e gli oggetti dello spazio dei nomi Search creati dall'indicizzatore.

## <a name="members"></a>Membri

**L'interfaccia ISearchItem** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISearchItem** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISearchItem** include questi metodi.



| Metodo                                                         | Descrizione                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentFolder**](-search-isearchitem-getparentfolder.md) | Ottiene **l'oggetto ISearchItem** se l'URL rappresenta un'origine dati Shell effettiva (nota anche come estensione dello spazio dei nomi Shell).<br/> |
| [**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | Ottiene l'oggetto dell'interfaccia utente di **ISearchItem.**<br/>                                                                        |



 

## <a name="remarks"></a>Commenti

[**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) è supportato solo in Windows XP e Windows Server 2003 e non deve più essere usato.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **ISearchItem** e le API seguenti: le interfacce [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI,**](-search-isearchprotocolui.md) la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



 

 
