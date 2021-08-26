---
description: La proprietà TablePersistent dell'oggetto Database restituisce lo stato di persistenza della tabella come uno dei parametri seguenti.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Database.TablePersistent - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f5eaf32996adef39976ba9fbaf88834c339e27dbe13c4e7fbcd1928ac1973b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129641"
---
# <a name="databasetablepersistent-property"></a>Database.TablePersistent - proprietà

La **proprietà TablePersistent** dell'oggetto [**Database**](database-object.md) restituisce lo stato di persistenza della tabella come uno dei parametri seguenti.



| Stato della tabella               | Valore | Descrizione                    |
|---------------------------|-------|--------------------------------|
| msiEvaluateConditionFalse | 0     | La tabella è temporanea.            |
| msiEvaluateConditionTrue  | 1     | La tabella è persistente.           |
| msiEvaluateConditionNone  | 2     | La tabella non è presente nel database.  |
| msiEvaluateConditionError | 3     | Nome di tabella non valido o mancante. |



 

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase è definito come \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




