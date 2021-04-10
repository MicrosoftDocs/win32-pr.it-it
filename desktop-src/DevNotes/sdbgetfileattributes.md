---
description: Recupera i dati dell'attributo per il file specificato.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes (funzione)
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
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125625"
---
# <a name="sdbgetfileattributes-function"></a>SdbGetFileAttributes (funzione)

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

*lpwszFileName* \[ in\]
</dt> <dd>

Percorso del file.

</dd> <dt>

*ppAttrInfo* \[ out\]
</dt> <dd>

Matrice di strutture [**ATTRINFO**](attrinfo.md) che contengono i dati dell'attributo.

</dd> <dt>

*lpdwAttrCount* \[ out\]
</dt> <dd>

Numero di attributi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="remarks"></a>Commenti

Una volta completati i dati, è possibile liberarli usando la funzione [**SdbFreeFileAttributes**](sdbfreefileattributes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




