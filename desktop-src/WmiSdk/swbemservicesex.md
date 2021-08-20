---
description: Estende le funzionalità di SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Oggetto SWbemServicesEx (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f7b63cbf6bc048350546b431b4f967c815450abf2d79c7ba79ab8f84e562a1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107839"
---
# <a name="swbemservicesex-object"></a>Oggetto SWbemServicesEx

**L'oggetto SWbemServicesEx** estende le funzionalità di [**SWbemServices.**](swbemservices.md) I [**metodi Put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) consentono di salvare una classe o un'istanza in più spazi dei nomi o in uno spazio dei nomi diverso da quello in cui è stata creata un'istanza. Questo oggetto non può essere creato dalla chiamata [createObject](/previous-versions//xzysf6hc(v=vs.85)) vbscript.

## <a name="members"></a>Membri

**L'oggetto SWbemServicesEx** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'oggetto SWbemServicesEx** include questi metodi.



| Metodo                                       | Descrizione                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mettere**](swbemservicesex-put.md)           | Salva l'oggetto nello spazio dei nomi associato all'oggetto **SWbemServicesEx** e restituisce un [**oggetto SWbemObjectPath**](swbemobjectpath.md) che contiene il percorso dell'oggetto in cui sono stati scritti i dati.<br/> |
| [**PutAsync**](swbemservicesex-putasync.md) | Salva un oggetto in modo asincrono in uno spazio dei nomi.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

I metodi in questa classe possono essere chiamati in modalità semisincrono o asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemServicesEx<br/>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> <dt>

[Chiamata di un metodo](calling-a-method.md)
</dt> </dl>

 

