---
description: Imposta il filtro BLOB Etype/Sap.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Funzione SetNPPEtypeSapFilter (Netmon.h)
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
ms.openlocfilehash: 30b2f6ffbefad955034f520162b6fdc44d80198d926f35443ce21fefd80ef5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363827"
---
# <a name="setnppetypesapfilter-function"></a>Funzione SetNPPEtypeSapFilter

La **funzione SetNPPEtypeSapFilter** imposta il filtro BLOB Etype/Sap.

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

*hBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*nSaps* \[ Pollici\]
</dt> <dd>

Numero di sap.

</dd> <dt>

*nEtypes* \[ Pollici\]
</dt> <dd>

Numero di Etype nella tabella Etype da impostare.

</dd> <dt>

*lpSapTable* \[ Pollici\]
</dt> <dd>

Puntatore alla tabella SAP impostata.

</dd> <dt>

*lpEtypeTable* \[ Pollici\]
</dt> <dd>

Puntatore alla tabella Etype impostata.

</dd> <dt>

*FilterFlags* \[ Pollici\]
</dt> <dd>

Flag di filtro impostati.

</dd> <dt>

*hErrorBlob* \[ Cambio\]
</dt> <dd>

Handle a un BLOB di errore che specifica dove nel BLOB originale si è verificato l'errore (se presente).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetNPPEtypeSapFilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




