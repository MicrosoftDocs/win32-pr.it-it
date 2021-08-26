---
description: Recupera il nome visualizzato dell'elemento TAG specificato.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: Funzione SdbTagToString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 22ddb526e332b335e88ecc7aaa770615220f6b0dde838386093e2813fe964e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044841"
---
# <a name="sdbtagtostring-function"></a>Funzione SdbTagToString

Recupera il nome visualizzato dell'elemento TAG specificato.

## <a name="syntax"></a>Sintassi


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tag* \[ Pollici\]
</dt> <dd>

The TAG.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un puntatore alla stringa con terminazione Null o a "InvalidTag".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TAG**](tag.md)
</dt> </dl>

 

 




