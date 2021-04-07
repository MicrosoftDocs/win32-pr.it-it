---
description: Crea un nuovo TAG di elenco per le operazioni di scrittura.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: SdbBeginWriteListTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748746"
---
# <a name="sdbbeginwritelisttag-function"></a>SdbBeginWriteListTag (funzione)

Crea un nuovo TAG di elenco per le operazioni di scrittura.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tTag* \[ in\]
</dt> <dd>

TAG per la nuova voce. Questo valore deve essere di tipo **\_ \_ elenco di tipi di tag**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce l' [**TagId**](tagid.md) del nuovo elenco in caso di esito positivo o **TagId \_ null** in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> <dt>

[**SdbEndWriteListTag**](sdbendwritelisttag.md)
</dt> <dt>

[**TAG**](tag.md)
</dt> <dt>

[Tipi di TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




