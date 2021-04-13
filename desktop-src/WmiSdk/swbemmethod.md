---
description: È possibile utilizzare le proprietà dell'oggetto SWbemMethod per controllare la definizione di un singolo metodo di un oggetto WMI. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Oggetto SWbemMethod (wbemdisp. h)
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
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528488"
---
# <a name="swbemmethod-object"></a>Oggetto SWbemMethod

È possibile utilizzare le proprietà dell'oggetto **SWbemMethod** per controllare la definizione di un singolo metodo di un oggetto WMI. Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.

Questo oggetto può essere utilizzato per controllare le definizioni dei metodi. Per richiamare i metodi, è consigliabile usare l'accesso diretto (vedere [modifica delle informazioni di classe e istanza](manipulating-class-and-instance-information.md)) in un oggetto [**SWbemObject**](swbemobject.md) (che è il meccanismo consigliato) o la chiamata [**cMethodSWbemServices.Exe**](swbemservices-execmethod.md) .

> [!Note]  
> In questa versione dell'API, l'accesso in scrittura alle informazioni sul metodo non è supportato. Se si desidera definire metodi o modificare definizioni di metodo esistenti, è possibile definire le modifiche al metodo in un file MOF e inviare le modifiche utilizzando il [compilatore MOF](compiling-mof-files.md). In alternativa, usare l' [API com per WMI](com-api-for-wmi.md).

 

## <a name="members"></a>Membri

L'oggetto **SWbemMethod** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **SWbemMethod** dispone di queste proprietà.



| Proprietà                                                      | Tipo di accesso          | Descrizione                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**InParameters**](swbemmethod-inparameters.md)<br/>   | Sola lettura<br/> | Oggetto [**SWbemObject**](swbemobject.md) le cui proprietà definiscono i parametri di input per questo metodo.<br/>              |
| [**Nome**](swbemmethod-name.md)<br/>                   | Sola lettura<br/> | Nome del metodo.<br/>                                                                                                     |
| [**Origine**](swbemmethod-origin.md)<br/>               | Sola lettura<br/> | Classe di origine del metodo.<br/>                                                                                        |
| [**OutParameters**](swbemmethod-outparameters.md)<br/> | Sola lettura<br/> | Oggetto [**SWbemObject**](swbemobject.md) le cui proprietà definiscono i parametri out e il tipo restituito di questo metodo.<br/> |
| [**Qualificatori\_**](swbemmethod-qualifiers-.md)<br/>    | Sola lettura<br/> | Oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) che contiene i qualificatori per questo metodo.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMMETHOD CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMMETHOD IID<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




