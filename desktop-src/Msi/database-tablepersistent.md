---
description: La proprietà TablePersistent dell'oggetto di database restituisce lo stato di persistenza della tabella come uno dei parametri seguenti.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Proprietà database. TablePersistent
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
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333054"
---
# <a name="databasetablepersistent-property"></a>Proprietà database. TablePersistent

La proprietà **TablePersistent** dell'oggetto di [**database**](database-object.md) restituisce lo stato di persistenza della tabella come uno dei parametri seguenti.



| Stato tabella               | Valore | Descrizione                    |
|---------------------------|-------|--------------------------------|
| msiEvaluateConditionFalse | 0     | Tabella temporanea.            |
| msiEvaluateConditionTrue  | 1     | Tabella persistente.           |
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
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




