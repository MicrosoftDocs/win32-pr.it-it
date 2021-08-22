---
description: Proietta una funzione rappresentata su una mappa del cubo in armonici sferici (SH).
ms.assetid: da5a3195-801e-4f1c-b52c-9eafc6e2e7b4
title: Funzione D3DXSHProjectCubeMap (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHProjectCubeMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7372eef528b90582d3aec64facb7c1aefffdfc479e97e1a5291f1a6d2feacc56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279471"
---
# <a name="d3dxshprojectcubemap-function"></a>Funzione D3DXSHProjectCubeMap

Proietta una funzione rappresentata su una mappa del cubo in armonici sferici (SH).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSHProjectCubeMap(
  _In_ UINT                   Order,
  _In_ LPDIRECT3DCUBETEXTURE9 pCubeMap,
  _In_ FLOAT                  *pROut,
  _In_ FLOAT                  *pGOut,
  _In_ FLOAT                  *pBOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione armonica sferica (SH). Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Order². Il grado di valutazione è Order - 1.

</dd> <dt>

*pCubeMap* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Puntatore a una trama del cubo di origine. Vedere [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).

</dd> <dt>

*pROut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente rosso.

</dd> <dt>

*pGOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente verde.

</dd> <dt>

*pBOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente blu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Trasferimento di radiance pre-ricalcolato (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
