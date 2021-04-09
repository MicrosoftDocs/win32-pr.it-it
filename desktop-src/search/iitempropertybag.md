---
description: Definisce i metodi per ottenere informazioni sulle proprietà di un elemento di ricerca. Questa interfaccia è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
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
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128503"
---
# <a name="iitempropertybag-interface"></a>Interfaccia IItemPropertyBag

Definisce i metodi per ottenere informazioni sulle proprietà di un elemento di ricerca. Questa interfaccia è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.

## <a name="members"></a>Membri

L'interfaccia **IItemPropertyBag** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IItemPropertyBag** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IItemPropertyBag** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Ottiene un conteggio del numero di proprietà nell'elenco delle proprietà.<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà.<br/> |
| [**Lettura**](iitempropertybag-read.md)                       | Determina la lettura di una o più proprietà dall'elenco delle proprietà.<br/>                   |
| [**Scrittura**](iitempropertybag-write.md)                     | Determina il salvataggio di una o più proprietà nel contenitore delle proprietà.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'interfaccia **IItemPropertyBag** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **IItemPropertyBag** e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem**](-search-isearchitem.md) , le strutture [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e l'enumerazione [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
