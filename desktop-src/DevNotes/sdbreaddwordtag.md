---
Description: Recupera il valore DWORD per il TAGID specificato.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: SdbReadDWORDTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121270"
---
# <a name="sdbreaddwordtag-function"></a>SdbReadDWORDTag (funzione)

Recupera il valore **DWORD** per il **TagId** specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
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

</dd> <dt>

*dwDefault* \[ in\]
</dt> <dd>

Valore predefinito da restituire in caso di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il valore in caso di esito positivo o *dwDefault* in caso di errore.

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

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




