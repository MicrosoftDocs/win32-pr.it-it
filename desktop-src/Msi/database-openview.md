---
description: Il metodo OpenView dell'oggetto Database restituisce un oggetto View che rappresenta la query specificata da una SQL stringa.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Metodo Database.OpenView (Certview.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ccc37b72dd44064172672d1067dae293da30048853f3ca83f82fb50b0a90cfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947524"
---
# <a name="databaseopenview-method"></a>Metodo Database.OpenView

Il **metodo OpenView** dell'oggetto [**Database**](database-object.md) restituisce un [**oggetto View**](view-object.md) che rappresenta la query specificata da una SQL stringa.

## <a name="syntax"></a>Sintassi


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sql* 
</dt> <dd>

Obbligatorio SQL stringa di query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per informazioni sulla sintassi SQL implementata nel programma di installazione, [vedere SQL Syntax](sql-syntax.md).

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| Intestazione<br/>  | <dl> <dt>Certview.h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Database**](database-object.md)
</dt> <dt>

[SQL Sintassi](sql-syntax.md)
</dt> </dl>

 

 




