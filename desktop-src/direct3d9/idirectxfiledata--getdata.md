---
description: Recupera i dati per uno dei membri dell'oggetto o i dati per tutti i membri. Deprecato.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'Metodo IDirectXFileData:: GetData (DXFile. h)'
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
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323232"
---
# <a name="idirectxfiledatagetdata-method"></a>Metodo IDirectXFileData:: GetData

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

*szMember* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome del membro per il quale recuperare i dati. Specificare **null** per recuperare tutti i dati necessari dei membri.

</dd> <dt>

*pcbSize* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore per la ricezione della dimensione del buffer ppvData in byte.

</dd> <dt>

*ppvData* \[ out\]
</dt> <dd>

Tipo: **void \* \***

Indirizzo di un puntatore al buffer per ricevere i dati associati a szMember. Se szMember è **null**, ppvData è impostato in modo da puntare a un buffer contenente tutti i dati necessari dei membri in un blocco di memoria contiguo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDATAREFERENCE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Questo metodo recupera i dati per i membri obbligatori di un oggetto dati, ma non i dati per i membri facoltativi (figlio). Usare [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) per recuperare oggetti figlio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
