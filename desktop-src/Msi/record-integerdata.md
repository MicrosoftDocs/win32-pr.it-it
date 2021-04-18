---
description: Si tratta della Proprietà IntegerData dell'oggetto record. Questa proprietà di lettura/scrittura trasferisce i dati Integer a 32 bit all'interno o all'esterno di un campo specificato all'interno del record. Se il valore di un campo non può essere convertito in un numero intero, viene restituito msiDatabaseNullInteger.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Proprietà record. IntegerData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328768"
---
# <a name="recordintegerdata-property"></a>Proprietà record. IntegerData

Si tratta della proprietà **IntegerData** dell'oggetto [**record**](record-object.md) . Questa proprietà di lettura/scrittura trasferisce i dati Integer a 32 bit all'interno o all'esterno di un campo specificato all'interno del record. Se il valore di un campo non può essere convertito in un numero intero, viene restituito msiDatabaseNullInteger.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Valore proprietà

Numero di campo obbligatorio del valore all'interno del record, basato su 1.

## <a name="remarks"></a>Commenti

Per impostare un campo record Integer su null, utilizzare msiDatabaseNullInteger. Il valore restituito di un campo inesistente è msiDatabaseNullInteger. Il tentativo di archiviare un valore in un campo inesistente causa un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




