---
description: La proprietà Item è una proprietà di sola lettura che restituisce un record in una raccolta di oggetti RecordList.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList.Item - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7df19a26fd4e8464963f09ffdf227ac88f4376624a88df84d6245efa3c5fd927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041811"
---
# <a name="recordlistitem-property"></a>RecordList.Item - proprietà

La **proprietà Item** è una proprietà di sola lettura che restituisce un record in una raccolta di oggetti [**RecordList.**](recordlist-object.md)

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>Valore proprietà

Numero di indice dell'elemento con la raccolta di stringhe. L'indice è obbligatorio.

## <a name="remarks"></a>Commenti

Il client deve verificare che [**l'oggetto RecordList**](recordlist-object.md) esista e non sia vuoto prima di fare riferimento alla proprietà Item.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecordList è definito come \_ 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




