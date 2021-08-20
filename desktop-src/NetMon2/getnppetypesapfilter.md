---
description: La funzione GetNPPEtypeSapFilter recupera il filtro Etype/Sap da un BLOB specificato.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Funzione GetNPPEtypeSapFilter (Netmon.h)
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
ms.openlocfilehash: 593030c3b53e7e11b20b9fe1497a3989b2ff68650d3d2df73f52e6491529d58e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982305"
---
# <a name="getnppetypesapfilter-function"></a>Funzione GetNPPEtypeSapFilter

La **funzione GetNPPEtypeSapFilter** recupera il filtro Etype/Sap da un BLOB specificato.

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

*hBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*pnSaps* \[ Cambio\]
</dt> <dd>

Puntatore al numero restituito di protocolli nella tabella SAP.

</dd> <dt>

*pnEtypes* \[ Cambio\]
</dt> <dd>

Puntatore al numero restituito di Etypes nella tabella Etype.

</dd> <dt>

*ppSapTable* \[ Cambio\]
</dt> <dd>

Puntatore alla tabella SAP restituita.

</dd> <dt>

*ppEtypeTable* \[ Cambio\]
</dt> <dd>

Puntatore alla tabella Etype restituita.

</dd> <dt>

*pFilterFlags* \[ Cambio\]
</dt> <dd>

Puntatore ai flag di filtro restituiti.

</dd> <dt>

*hErrorBlob* \[ Cambio\]
</dt> <dd>

Handle a un BLOB di errore, che specifica il percorso nel BLOB originale in cui si è verificato l'errore (se presente).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="remarks"></a>Commenti

Le informazioni Etype/Sap vengono archiviate nella **categoria Config (Configurazione)** della sezione NPP **Owner (Proprietario** NPP).

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

[SetNPPEtypeSapFilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




