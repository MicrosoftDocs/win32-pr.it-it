---
description: È possibile utilizzare le proprietà dell'oggetto oggetto SWbemQualifier per rappresentare un singolo qualificatore di una classe, un'istanza, una proprietà o un parametro di metodo WMI. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Oggetto oggetto SWbemQualifier (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226806"
---
# <a name="swbemqualifier-object"></a>Oggetto oggetto SWbemQualifier

È possibile utilizzare le proprietà dell'oggetto **oggetto SWbemQualifier** per rappresentare un singolo qualificatore di una classe, un'istanza, una proprietà o un parametro di metodo WMI. Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.

## <a name="members"></a>Membri

L'oggetto **oggetto SWbemQualifier** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **oggetto SWbemQualifier** dispone di queste proprietà.



| Proprietà                                                                       | Tipo di accesso           | Descrizione                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [**IsAmended**](swbemqualifier-isamended.md)<br/>                       | Sola lettura<br/>  | Valore booleano che indica se il qualificatore è stato localizzato utilizzando un'operazione di Unione.<br/> |
| [**IsLocal**](swbemqualifier-islocal.md)<br/>                           | Sola lettura<br/>  | Valore booleano che indica se il qualificatore è locale.<br/>                                   |
| [**IsOverridable**](swbemqualifier-isoverridable.md)<br/>               | Lettura/Scrittura<br/> | Valore booleano che indica se il qualificatore può essere sottoposto a override quando viene propagato.<br/>          |
| [**Nome**](swbemqualifier-name.md)<br/>                                 | Sola lettura<br/>  | Nome del qualificatore.<br/>                                                                    |
| [**PropagatesToInstance**](swbemqualifier-propagatestoinstance.md)<br/> | Lettura/Scrittura<br/> | Valore booleano che indica se il qualificatore può essere propagato a un'istanza.<br/>           |
| [**PropagatesToSubClass**](swbemqualifier-propagatestosubclass.md)<br/> | Sola lettura<br/>  | Valore booleano che indica se il qualificatore può essere propagato a una sottoclasse.<br/>            |
| [**Valore**](swbemqualifier-value.md)<br/>                               | Lettura/Scrittura<br/> | Valore Variant di questo qualificatore. Si tratta della proprietà predefinita di questo oggetto.<br/>              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_Oggetto SWBEMQUALIFIER CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMQUALIFIER IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




