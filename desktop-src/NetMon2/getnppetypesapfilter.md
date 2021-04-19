---
description: La funzione GetNPPEtypeSapFilter Recupera il filtro ETYPE/SAP da un BLOB specificato.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Funzione GetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319947"
---
# <a name="getnppetypesapfilter-function"></a>GetNPPEtypeSapFilter (funzione)

La funzione **GetNPPEtypeSapFilter** Recupera il filtro ETYPE/SAP da un blob specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*pnSaps* \[ out\]
</dt> <dd>

Puntatore al numero di protocolli restituito nella tabella SAP.

</dd> <dt>

*pnEtypes* \[ out\]
</dt> <dd>

Puntatore al numero restituito di ETYPE del nella tabella etype.

</dd> <dt>

*ppSapTable* \[ out\]
</dt> <dd>

Puntatore alla tabella SAP restituita.

</dd> <dt>

*ppEtypeTable* \[ out\]
</dt> <dd>

Puntatore alla tabella ETYPE restituita.

</dd> <dt>

*pFilterFlags* \[ out\]
</dt> <dd>

Puntatore ai flag di filtro restituiti.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle per un BLOB di errore, che specifica la posizione nel BLOB originale in cui si è verificato l'errore (se presente).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="remarks"></a>Commenti

Le informazioni su ETYPE/SAP sono archiviate nella categoria **config** della sezione del **proprietario** di NPP.

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

[SetNPPEtypeSapFilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




