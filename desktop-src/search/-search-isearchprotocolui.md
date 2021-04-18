---
description: Fornisce un metodo per richiamare gli oggetti ISearchItem.
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
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306159"
---
# <a name="isearchprotocolui-interface"></a>Interfaccia ISearchProtocolUI

Fornisce un metodo per richiamare gli oggetti [**ISearchItem**](-search-isearchitem.md) . I metodi in questa interfaccia vengono chiamati dall'host del protocollo durante l'elaborazione degli URL dal gatherer. Il gestore di protocollo implementa il protocollo per l'accesso a un'origine di contenuto nel formato nativo e questa interfaccia implementa un gestore di protocollo personalizzato per espandere le origini dati che possono essere indicizzate.

## <a name="members"></a>Membri

L'interfaccia **ISearchProtocolUI** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISearchProtocolUI** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISearchProtocolUI** dispone di questi metodi.



| Metodo                                                                       | Descrizione                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSearchItemForUrl**](-search-isearchprotocolui-getsearchitemforurl.md) | Ottiene l'elemento di ricerca per i dati specificati. Questo metodo viene chiamato una volta per ogni URL elaborato dal gatherer e recupera un puntatore all'oggetto [**ISearchItem**](-search-isearchitem.md) . <br/> |



 

## <a name="remarks"></a>Commenti

L'interfaccia **ISearchProtocolUI** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **ISearchProtocolUI** e le API seguenti: le interfacce [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
