---
description: Imposta il filtro ETYPE/SAP del BLOB.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Funzione SetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344961"
---
# <a name="setnppetypesapfilter-function"></a>SetNPPEtypeSapFilter (funzione)

La funzione **SetNPPEtypeSapFilter** imposta il filtro ETYPE/SAP del BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*nSaps* \[ in\]
</dt> <dd>

Numero di succhi.

</dd> <dt>

*nEtypes* \[ in\]
</dt> <dd>

Numero di ETYPE del nella tabella etype da impostare.

</dd> <dt>

*lpSapTable* \[ in\]
</dt> <dd>

Puntatore alla tabella SAP impostata.

</dd> <dt>

*lpEtypeTable* \[ in\]
</dt> <dd>

Puntatore alla tabella ETYPE impostata.

</dd> <dt>

*FilterFlags* \[ in\]
</dt> <dd>

Flag di filtro impostati.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle per un BLOB di errori che specifica il punto in cui si è verificato l'errore (se presente) nel BLOB originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetNPPEtypeSapFilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




