---
description: Recupera i dati per uno dei membri dell'oggetto o i dati per tutti i membri. Deprecato.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: Metodo IDirectXFileData::GetData (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 428bff1f3fd76cd7c4589d5084435f8a675ab0d73bf0ff02052b2212d2c2dea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728967"
---
# <a name="idirectxfiledatagetdata-method"></a>Metodo IDirectXFileData::GetData

Recupera i dati per uno dei membri dell'oggetto o i dati per tutti i membri. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szMember* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome del membro per il quale recuperare i dati. Specificare **NULL** per recuperare i dati di tutti i membri necessari.

</dd> <dt>

*pcbSize* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore per ricevere le dimensioni del buffer ppvData, in byte.

</dd> <dt>

*ppvData* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* void**

Indirizzo di un puntatore al buffer per ricevere i dati associati a szMember. Se szMember è **NULL,** ppvData è impostato in modo da puntare a un buffer contenente i dati di tutti i membri necessari in un blocco contiguo di memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDataReference, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Questo metodo recupera i dati per i membri obbligatori di un oggetto dati, ma nessun dato per i membri facoltativi (figlio). Usare [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) per recuperare gli oggetti figlio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
