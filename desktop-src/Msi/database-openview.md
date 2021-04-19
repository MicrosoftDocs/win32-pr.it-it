---
description: Il metodo OpenView dell'oggetto di database restituisce un oggetto visualizzazione che rappresenta la query specificata da una stringa SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Metodo database. OpenView (certview. h)
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
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333057"
---
# <a name="databaseopenview-method"></a>Metodo database. OpenView

Il metodo **OpenView** dell'oggetto di [**database**](database-object.md) restituisce un oggetto [**visualizzazione**](view-object.md) che rappresenta la query specificata da una stringa SQL.

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

Stringa di query SQL richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per informazioni sulla sintassi SQL implementata nel programma di installazione, vedere [sintassi SQL](sql-syntax.md).

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| Intestazione<br/>  | <dl> <dt>Certview. h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Database**](database-object.md)
</dt> <dt>

[Sintassi SQL](sql-syntax.md)
</dt> </dl>

 

 




