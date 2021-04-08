---
description: Un oggetto dell'SWbemQualifierSet è una raccolta di oggetti oggetto SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Oggetto dell'SWbemQualifierSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058262"
---
# <a name="swbemqualifierset-object"></a>Oggetto dell'SWbemQualifierSet

Un oggetto **dell'SWbemQualifierSet** è una raccolta di oggetti [**oggetto SWbemQualifier**](swbemqualifier.md) . Gli elementi vengono aggiunti alla raccolta usando il metodo [**Add**](swbemqualifierset-add.md) , recuperati dalla raccolta usando il metodo [**Item**](swbemqualifierset-item.md) e rimossi dalla raccolta usando il metodo [**Remove**](swbemqualifierset-remove.md) . Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.

Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).

Gli oggetti [**oggetto SWbemQualifier**](swbemqualifier.md) che costituiscono una raccolta **dell'SWbemQualifierSet** descrivono i qualificatori associati a una classe WMI, un'istanza, un metodo o un parametro del metodo.

## <a name="members"></a>Membri

L'oggetto **dell'SWbemQualifierSet** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **dell'SWbemQualifierSet** dispone di questi metodi.



| Metodo                                     | Descrizione                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](swbemqualifierset-add.md)       | Aggiunge un oggetto [**oggetto SWbemQualifier**](swbemqualifier.md) alla raccolta **dell'SWbemQualifierSet** .<br/> |
| [**Elemento**](swbemqualifierset-item.md)     | Restituisce un oggetto denominato [**oggetto SWbemQualifier**](swbemqualifier.md) dalla raccolta.<br/>             |
| [**Rimuovi**](swbemqualifierset-remove.md) | Elimina un qualificatore denominato dalla raccolta.<br/>                                                   |



 

### <a name="properties"></a>Proprietà

L'oggetto **dell'SWbemQualifierSet** dispone di queste proprietà.



| Proprietà                                            | Tipo di accesso          | Descrizione                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**Conteggio**](swbemqualifierset-count.md)<br/> | Sola lettura<br/> | Contiene il numero di elementi in una raccolta **dell'SWbemQualifierSet** .<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_Dell'SWBEMQUALIFIERSET CLSID<br/>                                                     |
| IID<br/>                      | \_ISWBEMQUALIFIERSET IID<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




