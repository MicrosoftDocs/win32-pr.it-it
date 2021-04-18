---
description: Recupera un puntatore al nome di un oggetto file DirectX. Deprecato.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'Metodo IDirectXFileObject:: GetName (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322534"
---
# <a name="idirectxfileobjectgetname-method"></a>Metodo IDirectXFileObject:: GetName

Recupera un puntatore al nome di un oggetto file DirectX. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstrNameBuf* \[ out\]
</dt> <dd>

Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**

Puntatore al buffer in cui verrà copiato il nome dell'oggetto file DirectX. Impostare su **null** se è necessaria solo la lunghezza del buffer.

</dd> <dt>

*pdwBufLen* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Puntatore a un valore DWORD che specifica la lunghezza del buffer a cui punta pstrNameBuf. Il valore del parametro pdwBufLen verrà modificato in base alla lunghezza del buffer necessaria per contenere il nome dell'oggetto anche se pstrNameBuf è **null**. In entrambi i casi, la funzione restituirà DXFILEERR \_ BADVALUE se il valore originale di pdwBufLen non è grande o maggiore della lunghezza necessaria per conservare il nome dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 
