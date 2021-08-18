---
description: È possibile usare le proprietà dell'oggetto SWbemMethod per esaminare una singola definizione di metodo di un oggetto WMI. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Oggetto SWbemMethod (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c750e81a3e41450e8cd32f37ccab6fee2f08439c6bc8fc8ae18bf0e4f106b551
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732661"
---
# <a name="swbemmethod-object"></a>Oggetto SWbemMethod

È possibile usare le proprietà **dell'oggetto SWbemMethod** per esaminare una singola definizione di metodo di un oggetto WMI. Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.

Questo oggetto può essere usato per esaminare le definizioni dei metodi. Per richiamare i metodi, è necessario usare l'accesso diretto (vedere Modifica delle informazioni sulla classe e sull'istanza [)](manipulating-class-and-instance-information.md)su un [**oggetto SWbemObject**](swbemobject.md) (che è il meccanismo consigliato) o la chiamataSWbemServices.Exe [**cMethod.**](swbemservices-execmethod.md)

> [!Note]  
> In questa versione dell'API l'accesso in scrittura alle informazioni sul metodo non è supportato. Se si vogliono definire metodi o modificare definizioni di metodi esistenti, è possibile definire le modifiche ai metodi in un file MOF e inviare le modifiche usando il compilatore [MOF](compiling-mof-files.md). In alternativa, usare [l'API COM per WMI.](com-api-for-wmi.md)

 

## <a name="members"></a>Membri

**L'oggetto SWbemMethod** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto SWbemMethod** ha queste proprietà.



| Proprietà                                                      | Tipo di accesso          | Descrizione                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**InParameters**](swbemmethod-inparameters.md)<br/>   | Sola lettura<br/> | Oggetto [**SWbemObject le**](swbemobject.md) cui proprietà definiscono i parametri di input per questo metodo.<br/>              |
| [**Nome**](swbemmethod-name.md)<br/>                   | Sola lettura<br/> | Nome del metodo.<br/>                                                                                                     |
| [**Origine**](swbemmethod-origin.md)<br/>               | Sola lettura<br/> | Classe di origine del metodo.<br/>                                                                                        |
| [**OutParameters**](swbemmethod-outparameters.md)<br/> | Sola lettura<br/> | Oggetto [**SWbemObject le**](swbemobject.md) cui proprietà definiscono i parametri out e il tipo restituito di questo metodo.<br/> |
| [**Qualificatori\_**](swbemmethod-qualifiers-.md)<br/>    | Sola lettura<br/> | Oggetto [**SWbemQualifierSet**](swbemqualifierset.md) che contiene i qualificatori per questo metodo.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

 




