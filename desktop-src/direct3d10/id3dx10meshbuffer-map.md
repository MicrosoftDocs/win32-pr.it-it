---
description: Ottenere un puntatore alla memoria del buffer mesh per modificarne il contenuto.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'Metodo ID3DX10MeshBuffer:: Map (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354944"
---
# <a name="id3dx10meshbuffermap-method"></a>Metodo ID3DX10MeshBuffer:: Map

Ottenere un puntatore alla memoria del buffer mesh per modificarne il contenuto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **void \* \***

Puntatore ai dati del buffer.

</dd> <dt>

*psize* \[ out\]
</dt> <dd>

Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)\***

Dimensione del buffer in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> Map () in Direct3D 10 è analogo alla mappa delle risorse () in Direct3D 9.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
