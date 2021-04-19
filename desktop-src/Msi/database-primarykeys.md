---
description: La proprietà PrimaryKeys dell'oggetto di database restituisce un oggetto record contenente il nome della tabella nel campo 0 e i nomi di colonna (che includono le chiavi primarie) nei campi successivi corrispondenti ai numeri di colonna.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Proprietà database. PrimaryKeys
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333056"
---
# <a name="databaseprimarykeys-property"></a>Proprietà database. PrimaryKeys

La proprietà **PrimaryKeys** dell'oggetto di [**database**](database-object.md) restituisce un oggetto [**record**](record-object.md) contenente il nome della tabella nel campo 0 e i nomi di colonna (che includono le chiavi primarie) nei campi successivi corrispondenti ai numeri di colonna. Il numero di campi del record è il numero di colonne chiave primaria.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a>Valore proprietà

Nome obbligatorio di una tabella esistente. Se la tabella non esiste, viene generato un errore.

## <a name="remarks"></a>Commenti

Impossibile utilizzare la proprietà **PrimaryKeys** con [ \_ la tabella Tables o](-tables-table.md) [ \_ Columns](-columns-table.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




