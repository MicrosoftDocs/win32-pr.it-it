---
description: Fornisce funzionalità estese per SWbemObject. Analogamente a SWbemObject, i metodi di questo oggetto esteso possono essere utilizzati da tutti gli oggetti WMI.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: Oggetto SWbemObjectEx (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: abed8c1d58687203aaeb32918cf15b2785b92622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309811"
---
# <a name="swbemobjectex-object"></a>Oggetto SWbemObjectEx

L'oggetto **SWbemObjectEx** fornisce funzionalità estese per [**SWbemObject**](swbemobject.md). Analogamente a **SWbemObject**, i metodi di questo oggetto esteso possono essere utilizzati da tutti gli oggetti WMI. Questo oggetto non può essere creato dalla chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemObjectEx** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemObjectEx** dispone di questi metodi.



| Metodo                                      | Descrizione                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [**GetText\_**](swbemobjectex-gettext-.md) | Restituisce un file di testo che mostra il contenuto di un oggetto in XML.<br/> |
| [**Aggiorna\_**](swbemobjectex-refresh-.md) | Aggiorna i dati in un oggetto.<br/>                                  |
| **SetFromText\_**                           | Riservato per utilizzi futuri.<br/>                                      |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemObjectEx** dispone di queste proprietà.



| Proprietà                                                                 | Tipo di accesso           | Descrizione                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SystemProperties\_**](swbemobjectex-systemproperties-.md)<br/> | Lettura/Scrittura<br/> | Oggetto [**SWbemPropertySet**](swbempropertyset.md) che contiene la raccolta di proprietà di sistema che si applicano a **SWbemObjectEx**.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTEX CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMOBJECTEX IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[WbemObjectTextFormatEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

