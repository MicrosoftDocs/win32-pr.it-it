---
description: Fornisce metodi per fornire le impostazioni del browser. L'interfaccia IItemPreviewerExt è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Interfaccia IItemPreviewerExt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966534"
---
# <a name="iitempreviewerext-interface"></a>Interfaccia IItemPreviewerExt

Fornisce metodi per fornire le impostazioni del browser. L'interfaccia **IItemPreviewerExt** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

## <a name="members"></a>Membri

L'interfaccia **IItemPreviewerExt** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IItemPreviewerExt** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IItemPreviewerExt** dispone di questi metodi.



| Metodo                                                                               | Descrizione                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md)               | Consente all'estensione di contenuti avanzati per una proprietà. <br/>                            |
| [**GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md)                   | Ottiene una parte del corpo correlata per l'incorporamento nel flusso MHTML di output.<br/>              |
| [**ProcessTransformCommand**](-search-iitempreviewerext-processtransformcommand.md) | Consente l'elaborazione di un comando di trasformazione rilevato in un modello di anteprima.<br/> |
| [**SuggestBrowserPolicy**](-search-iitempreviewerext-suggestbrowserpolicy.md)       | Suggerisce che i criteri di sicurezza devono essere applicati al browser.<br/>                        |



 

## <a name="remarks"></a>Commenti

L'interfaccia **IItemPreviewerExt** è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia **IItemPreviewerExt** e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
