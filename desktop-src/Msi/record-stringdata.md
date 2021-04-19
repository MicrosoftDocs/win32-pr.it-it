---
description: La proprietà StringData dell'oggetto record è una proprietà di lettura/scrittura che trasferisce i dati stringa in o da un campo specificato all'interno del record. Se è stato archiviato un intero o un oggetto, viene restituito il relativo valore stringa.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Proprietà record. StringData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328762"
---
# <a name="recordstringdata-property"></a>Proprietà record. StringData

La proprietà **StringData** dell'oggetto [**record**](record-object.md) è una proprietà di lettura/scrittura che trasferisce i dati stringa in o da un campo specificato all'interno del record. Se è stato archiviato un intero o un oggetto, viene restituito il relativo valore stringa.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a>Valore proprietà

Numero di campo obbligatorio del valore all'interno del record, basato su 1.

## <a name="remarks"></a>Commenti

Il valore restituito di un campo inesistente è una stringa vuota. Per impostare un campo della stringa di record su null, utilizzare una stringa Variant vuota o vuota. Il tentativo di archiviare un valore in un campo inesistente causa un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




