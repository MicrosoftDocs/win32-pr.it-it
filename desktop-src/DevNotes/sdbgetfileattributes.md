---
description: Recupera i dati dell'attributo per il file specificato.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: Funzione SdbGetFileAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a75dd64bfbeaf027839c63227c594ada7602101d059cbbd9d10deb085152918d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103651"
---
# <a name="sdbgetfileattributes-function"></a>Funzione SdbGetFileAttributes

Recupera i dati dell'attributo per il file specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpwszFileName* \[ Pollici\]
</dt> <dd>

Percorso del file.

</dd> <dt>

*ppAttrInfo* \[ Cambio\]
</dt> <dd>

Matrice di strutture [**ATTRINFO**](attrinfo.md) che contengono i dati dell'attributo.

</dd> <dt>

*lpdwAttrCount* \[ Cambio\]
</dt> <dd>

Numero di attributi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di esito negativo.

## <a name="remarks"></a>Commenti

Al termine, liberare i dati usando la [**funzione SdbFreeFileAttributes.**](sdbfreefileattributes.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




