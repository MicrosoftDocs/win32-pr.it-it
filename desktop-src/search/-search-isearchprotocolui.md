---
description: Fornisce un metodo per richiamare oggetti ISearchItem.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Interfaccia ISearchProtocolUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4794c0a2de43c08645af5ea7d44d0dbd872fe6fc88c33f5fcdb830955fc594be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463016"
---
# <a name="isearchprotocolui-interface"></a>Interfaccia ISearchProtocolUI

Fornisce un metodo per richiamare oggetti [**ISearchItem.**](-search-isearchitem.md) I metodi in questa interfaccia vengono chiamati dall'host del protocollo durante l'elaborazione degli URL dal gatherer. Il gestore di protocollo implementa il protocollo per l'accesso a un'origine contenuto nel formato nativo e questa interfaccia implementa un gestore di protocollo personalizzato per espandere le origini dati che possono essere indicizzate.

## <a name="members"></a>Membri

**L'interfaccia ISearchProtocolUI** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISearchProtocolUI** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISearchProtocolUI** include questi metodi.



| Metodo                                                                       | Descrizione                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSearchItemForUrl**](-search-isearchprotocolui-getsearchitemforurl.md) | Ottiene l'elemento di ricerca per i dati specificati. Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore [**all'oggetto ISearchItem.**](-search-isearchitem.md) <br/> |



 

## <a name="remarks"></a>Commenti

**L'interfaccia ISearchProtocolUI** è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **ISearchProtocolUI** e le API seguenti: le interfacce [**IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



 

 
