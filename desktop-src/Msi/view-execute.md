---
description: Il metodo Execute dell'oggetto View usa il token Question Mark per rappresentare i parametri in un'istruzione SQL. Per altre informazioni, vedere Sintassi SQL. I valori di questi parametri vengono passati come campi corrispondenti di un record di parametri.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exemetodo carino
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
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324769"
---
# <a name="viewexecute-method"></a>View.Exemetodo carino

Il metodo **Execute** dell'oggetto [**View**](view-object.md) usa il token Question Mark per rappresentare i parametri in un'istruzione SQL. Per altre informazioni, vedere [sintassi SQL](sql-syntax.md). I valori di questi parametri vengono passati come campi corrispondenti di un record di parametri.

## <a name="syntax"></a>Sintassi


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*record* 
</dt> <dd>

Oggetti [**record**](record-object.md) facoltativi che contengono i valori che sostituiscono i token di parametro (?) nella query SQL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato prima di qualsiasi chiamata al metodo [**Fetch**](view-fetch.md) .

Se la query SQL specifica valori con marcatori di parametro (?), è necessario specificare un record contenente tutti i valori di sostituzione, che devono essere nello stesso ordine e dello stesso tipo di dati dei marcatori di parametro. Quando questo metodo viene utilizzato con le query di inserimento e aggiornamento, i token dei punti interrogativi devono precedere tutti i valori senza parametri.

Ad esempio, queste query sono valide:

AGGIORNAMENTO {Table-list} SET {Column} =? , {Column} = {Constant}

INSERT INTO {TABLE} ({Column-List}) valori (?, {Constant-List})

Tuttavia, queste query non sono valide:

AGGIORNAMENTO {Table-list} SET {Column} = {Constant}, {Column} =?

INSERIRE i valori {Table} ({Column-List}) ({Constant-list},? )

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




