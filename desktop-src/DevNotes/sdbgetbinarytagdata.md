---
description: Recupera i dati binari per il TAGID specificato.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: SdbGetBinaryTagData (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304652"
---
# <a name="sdbgetbinarytagdata-function"></a>SdbGetBinaryTagData (funzione)

Recupera i dati binari per il **TagId** specificato.

## <a name="syntax"></a>Sintassi


```C++
PVOID WINAPI SdbGetBinaryTagData(
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

**TagId** che corrisponde ai dati da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un puntatore ai dati binari o **null** se **TagId** non è valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




