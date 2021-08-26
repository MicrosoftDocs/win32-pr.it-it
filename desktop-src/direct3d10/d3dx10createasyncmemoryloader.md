---
description: Creare un caricatore di memoria asincrona.
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: Funzione D3DX10CreateAsyncMemoryLoader (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 897977147157c754c0f0da1c68e5e64b3fa64ea792c573c1f901aca6aec433fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989231"
---
# <a name="d3dx10createasyncmemoryloader-function"></a>Funzione D3DX10CreateAsyncMemoryLoader

Creare un caricatore di memoria asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore ai dati.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Dimensioni dei dati.

</dd> <dt>

*ppDataLoader* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Indirizzo di un puntatore al processore di dati asincrono (vedere [**l'interfaccia ID3DX10DataProcessor).**](id3dx10dataprocessor.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
