---
description: L'oggetto SWbemProperty rappresenta una singola proprietà WMI di un oggetto gestito. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Oggetto SWbemProperty (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233986"
---
# <a name="swbemproperty-object"></a>Oggetto SWbemProperty

L'oggetto **SWbemProperty** rappresenta una singola proprietà WMI di un oggetto gestito. Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemProperty** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **SWbemProperty** dispone di queste proprietà.



| Proprietà                                                     | Tipo di accesso           | Descrizione                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**CIMType**](swbemproperty-cimtype.md)<br/>          | Sola lettura<br/>  | Tipo di questa proprietà.<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | Sola lettura<br/>  | Valore booleano che indica se questa proprietà ha un tipo di matrice.<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | Sola lettura<br/>  | Valore booleano che indica se questa proprietà è locale.<br/>                                                            |
| [**Nome**](swbemproperty-name.md)<br/>                | Sola lettura<br/>  | Nome della proprietà WMI.<br/>                                                                                         |
| [**Origine**](swbemproperty-origin.md)<br/>            | Sola lettura<br/>  | Contiene la classe di origine di questa proprietà.<br/>                                                                   |
| [**Qualificatori\_**](swbemproperty-qualifiers-.md)<br/> | Sola lettura<br/>  | Oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) , ovvero la raccolta di qualificatori per questa proprietà.<br/> |
| [**Valore**](swbemproperty-value.md)<br/>              | Lettura/Scrittura<br/> | Valore effettivo della proprietà. Si tratta della proprietà di automazione predefinita di questo oggetto.<br/>                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMPROPERTY IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




