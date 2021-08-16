---
description: Definisce i metodi per ottenere informazioni sulle proprietà di un elemento di ricerca. Questa interfaccia è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Interfaccia IItemPropertyBag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2657fea53c4e7021e17df4b74cc210bd8547180566ff579524f85b7663a0c247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226562"
---
# <a name="iitempropertybag-interface"></a>Interfaccia IItemPropertyBag

Definisce i metodi per ottenere informazioni sulle proprietà di un elemento di ricerca. Questa interfaccia è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

## <a name="members"></a>Membri

**L'interfaccia IItemPropertyBag** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IItemPropertyBag** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IItemPropertyBag** include questi metodi.



| Metodo                                                      | Descrizione                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Ottiene un conteggio del numero di proprietà nell'elenco delle proprietà.<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà.<br/> |
| [**Leggere**](iitempropertybag-read.md)                       | Fa sì che una o più proprietà siano lette dal contenitore delle proprietà.<br/>                   |
| [**Scrivere**](iitempropertybag-write.md)                     | Determina il salvataggio di una o più proprietà nel contenitore delle proprietà.<br/>                  |



 

## <a name="remarks"></a>Commenti

**L'interfaccia IItemPropertyBag** è supportata solo in Windows XP e Windows Server 2003 e non deve più essere usata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **IItemPropertyBag** e le API seguenti: le interfacce [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem,**](-search-isearchitem.md) le strutture [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



 

 
