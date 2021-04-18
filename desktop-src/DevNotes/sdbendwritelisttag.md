---
description: Termina le operazioni di scrittura per l'elenco specificato.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: SdbEndWriteListTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304404"
---
# <a name="sdbendwritelisttag-function"></a>SdbEndWriteListTag (funzione)

Termina le operazioni di scrittura per l'elenco specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDB* \[ in uscita\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tiList* \[ in\]
</dt> <dd>

[**TagId**](tagid.md) dell'elenco

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="remarks"></a>Commenti

Chiamare questa funzione dopo la scrittura di tutte le voci dell'elenco; verrà contrassegnata la fine dell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
</dt> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




