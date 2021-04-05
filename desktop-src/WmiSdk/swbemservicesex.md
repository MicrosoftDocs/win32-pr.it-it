---
description: Estende la funzionalità di SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Oggetto SWbemServicesEx (wbemdisp. h)
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
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130971"
---
# <a name="swbemservicesex-object"></a>Oggetto SWbemServicesEx

L'oggetto **SWbemServicesEx** estende la funzionalità di [**SWbemServices**](swbemservices.md). I metodi [**put**](swbemservicesex-put.md) e [**PutAsync**](swbemservicesex-putasync.md) consentono il salvataggio di una classe o di un'istanza in più spazi dei nomi o in uno spazio dei nomi diverso da quello in cui è stata creata un'istanza. Questo oggetto non può essere creato dalla chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemServicesEx** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **SWbemServicesEx** dispone di questi metodi.



| Metodo                                       | Descrizione                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Mettere**](swbemservicesex-put.md)           | Salva l'oggetto nello spazio dei nomi associato all'oggetto **SWbemServicesEx** e restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che contiene il percorso dell'oggetto in cui sono stati scritti i dati.<br/> |
| [**PutAsync**](swbemservicesex-putasync.md) | Salva un oggetto in modo asincrono in uno spazio dei nomi.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

I metodi di questa classe possono essere chiamati sia in modalità semisincrono che in modalità asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_ISWBEMSERVICESEX CLSID<br/>                                                      |
| IID<br/>                      | \_ISWBEMSERVICESEX IID<br/>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

