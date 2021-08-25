---
description: La proprietà DatabaseState dell'oggetto Database è una proprietà di sola lettura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Database.DatabaseState - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a44fcc9e082878077533edafcd44c9f5a5f26e76bddd3ddb5619fb2842ec0d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745641"
---
# <a name="databasedatabasestate-property"></a>Database.DatabaseState - proprietà

La **proprietà DatabaseState** dell'oggetto [**Database**](database-object.md) è una proprietà di sola lettura.

Questa proprietà restituisce lo stato di persistenza del database come uno dei parametri seguenti.



| Stato del database        | Valore | Descrizione                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| msiDatabaseStateRead  | 0     | Il database viene aperto in sola lettura. Le modifiche ai dati permanenti non sono consentite e i dati temporanei non vengono salvati. |
| msiDatabaseStateWrite | 1     | Il database è completamente operativo per la lettura e la scrittura.                                                          |



 

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




