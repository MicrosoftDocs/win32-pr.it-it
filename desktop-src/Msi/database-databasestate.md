---
description: La proprietà DatabaseState dell'oggetto di database è una proprietà di sola lettura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Proprietà database. DatabaseState
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
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326545"
---
# <a name="databasedatabasestate-property"></a>Proprietà database. DatabaseState

La proprietà **DatabaseState** dell'oggetto di [**database**](database-object.md) è una proprietà di sola lettura.

Questa proprietà restituisce lo stato di persistenza del database come uno dei parametri seguenti.



| Stato del database        | Valore | Descrizione                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| msiDatabaseStateRead  | 0     | Il database viene aperto in sola lettura. Le modifiche ai dati persistenti non sono consentite e i dati temporanei non vengono salvati. |
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
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




