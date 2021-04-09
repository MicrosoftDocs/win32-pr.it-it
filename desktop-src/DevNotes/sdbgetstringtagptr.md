---
description: Recupera i dati di stringa per il TAGID specificato.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: SdbGetStringTagPtr (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966115"
---
# <a name="sdbgetstringtagptr-function"></a>SdbGetStringTagPtr (funzione)

Recupera i dati di stringa per il **TagId** specificato.

## <a name="syntax"></a>Sintassi


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tiWhich* \[ in\]
</dt> <dd>

**TagId** che corrisponde ai dati stringa da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un puntatore ai dati di tipo stringa o **null** se **TagId** non è valido o non è di tipo **\_ \_ stringa** o **tipo di tag \_ \_ STRINGREF**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




