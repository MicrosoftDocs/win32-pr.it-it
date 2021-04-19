---
description: La proprietà DataSize dell'oggetto record è una proprietà di sola lettura che restituisce la dimensione dei dati per il campo designato.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Proprietà record. DataSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328772"
---
# <a name="recorddatasize-property"></a>Proprietà record. DataSize

La proprietà **DataSize** dell'oggetto [**record**](record-object.md) è una proprietà di sola lettura che restituisce la dimensione dei dati per il campo designato. Se i dati sono un flusso, viene restituita la lunghezza del flusso in byte. Se i dati sono una stringa, viene restituita la lunghezza della stringa senza null. Se i dati sono di tipo Integer, viene restituito il valore 4 (che indica le dimensioni dell'Integer). Se i dati sono null, viene restituito 0.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Valore proprietà

Numero di campo obbligatorio del valore all'interno del record, basato su 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




