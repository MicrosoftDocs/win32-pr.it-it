---
description: Il metodo Execute dell'oggetto View usa il token punto interrogativo per rappresentare i parametri in un SQL istruzione . Per altre informazioni, vedere Sintassi SQL. I valori di questi parametri vengono passati come campi corrispondenti di un record di parametro.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exemetodo method
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9bfd1120382ea06f6046f4435d0143024422ff6345959099326ab4a5428d26d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804029"
---
# <a name="viewexecute-method"></a>View.Exemetodo method

Il **metodo Execute** dell'oggetto [**View**](view-object.md) usa il token punto interrogativo per rappresentare i parametri in un SQL istruzione . Per altre informazioni, vedere [Sintassi SQL.](sql-syntax.md) I valori di questi parametri vengono passati come campi corrispondenti di un record di parametro.

## <a name="syntax"></a>Sintassi


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Registrazione* 
</dt> <dd>

Oggetti [**Record**](record-object.md) facoltativi che contengono i valori che sostituiscono i token di parametro (?) nella query SQL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato prima di qualsiasi chiamata al [**metodo Fetch.**](view-fetch.md)

Se la query SQL specifica valori con marcatori di parametro (?), è necessario specificare un record contenente tutti i valori di sostituzione, che devono essere nello stesso ordine e dello stesso tipo di dati dei marcatori di parametro. Quando questo metodo viene utilizzato con query INSERT e UPDATE, i token punto interrogativo devono precedere tutti i valori senza parametri.

Ad esempio, queste query sono valide:

UPDATE {table-list} SET {column}= ? , {column}= {constant}

INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})

Queste query non sono tuttavia valide:

UPDATE {table-list} SET {column}= {constant}, {column}=?

INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ? )

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




