---
description: Scrive dati binari nel database specificato.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: Funzione SdbWriteBinaryTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 06900cf49445b52c519b04f88ffc6d5b3ba539404bf64bd7f820a502f70ec2e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044851"
---
# <a name="sdbwritebinarytag-function"></a>Funzione SdbWriteBinaryTag

Scrive dati binari nel database specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdb* \[ Pollici\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tTag* \[ Pollici\]
</dt> <dd>

TAG per la voce. Questo TAG deve essere di tipo **TAG \_ TYPE \_ BINARY.**

</dd> <dt>

*pBuffer* \[ Pollici\]
</dt> <dd>

Buffer che contiene i dati. Questo parametro non può essere **NULL.**

</dd> <dt>

*dwSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *pBuffer,* in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
</dt> <dt>

[**SdbWriteStringTag**](sdbwritestringtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 




