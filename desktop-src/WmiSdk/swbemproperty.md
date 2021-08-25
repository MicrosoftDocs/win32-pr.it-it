---
description: L'oggetto SWbemProperty rappresenta una singola proprietà WMI di un oggetto gestito. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Oggetto SWbemProperty (Wbemdisp.h)
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
ms.openlocfilehash: 51f4b1b22849fc5a6ae22f49c5c30411563efb9d133cf2440c301eabfde18e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898071"
---
# <a name="swbemproperty-object"></a>Oggetto SWbemProperty

**L'oggetto SWbemProperty** rappresenta una singola proprietà WMI di un oggetto gestito. Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.

## <a name="members"></a>Membri

**L'oggetto SWbemProperty** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto SWbemProperty** ha queste proprietà.



| Proprietà                                                     | Tipo di accesso           | Descrizione                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**Cimtype**](swbemproperty-cimtype.md)<br/>          | Sola lettura<br/>  | Tipo di questa proprietà.<br/>                                                                                             |
| [**Isarray**](swbemproperty-isarray.md)<br/>          | Sola lettura<br/>  | Valore booleano che indica se questa proprietà ha un tipo di matrice.<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | Sola lettura<br/>  | Valore booleano che indica se questa proprietà è locale.<br/>                                                            |
| [**Nome**](swbemproperty-name.md)<br/>                | Sola lettura<br/>  | Nome di questa proprietà WMI.<br/>                                                                                         |
| [**Origine**](swbemproperty-origin.md)<br/>            | Sola lettura<br/>  | Contiene la classe di origine di questa proprietà.<br/>                                                                   |
| [**Qualificatori\_**](swbemproperty-qualifiers-.md)<br/> | Sola lettura<br/>  | Oggetto [**SWbemQualifierSet,**](swbemqualifierset.md) ovvero la raccolta di qualificatori per questa proprietà.<br/> |
| [**Valore**](swbemproperty-value.md)<br/>              | Lettura/Scrittura<br/> | Valore effettivo di questa proprietà. Si tratta della proprietà di automazione predefinita di questo oggetto.<br/>                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

 




