---
description: Un oggetto SWbemQualifierSet è una raccolta di oggetti SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Oggetto SWbemQualifierSet (Wbemdisp.h)
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
ms.openlocfilehash: 1ed8ec4c244c2ecc2ab2f14200744d4f6d7c78a7891638b96e0b2efb71c408ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921980"
---
# <a name="swbemqualifierset-object"></a>Oggetto SWbemQualifierSet

Un **oggetto SWbemQualifierSet** è una raccolta di [**oggetti SWbemQualifier.**](swbemqualifier.md) Gli elementi vengono aggiunti alla raccolta usando il [**metodo Add,**](swbemqualifierset-add.md) recuperati dalla raccolta usando il [**metodo Item**](swbemqualifierset-item.md) e rimossi dalla raccolta usando il [**metodo Remove.**](swbemqualifierset-remove.md) Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.

Per altre informazioni, vedere [Accesso a una raccolta](accessing-a-collection.md).

Gli [**oggetti SWbemQualifier**](swbemqualifier.md) che costituiscono una raccolta **SWbemQualifierSet** descrivono i qualificatori associati a una classe, un'istanza, un metodo o un parametro del metodo WMI.

## <a name="members"></a>Membri

**L'oggetto SWbemQualifierSet** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SWbemQualifierSet** dispone di questi metodi.



| Metodo                                     | Descrizione                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](swbemqualifierset-add.md)       | Aggiunge un [**oggetto SWbemQualifier**](swbemqualifier.md) alla **raccolta SWbemQualifierSet.**<br/> |
| [**Elemento**](swbemqualifierset-item.md)     | Restituisce un [**oggetto SWbemQualifier**](swbemqualifier.md) denominato dalla raccolta.<br/>             |
| [**Rimuovi**](swbemqualifierset-remove.md) | Elimina un qualificatore denominato dalla raccolta.<br/>                                                   |



 

### <a name="properties"></a>Proprietà

**L'oggetto SWbemQualifierSet** ha queste proprietà.



| Proprietà                                            | Tipo di accesso          | Descrizione                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**Conteggio**](swbemqualifierset-count.md)<br/> | Sola lettura<br/> | Contiene il numero di elementi in una **raccolta SWbemQualifierSet.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

 




