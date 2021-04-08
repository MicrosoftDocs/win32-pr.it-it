---
description: Estrae i dati coefficienti da un canale colori del buffer per un intervallo di coefficienti specificato e aggiunge i dati a un oggetto IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'Metodo ID3DXPRTBuffer:: ExtractTexture (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969404"
---
# <a name="id3dxprtbufferextracttexture-method"></a>Metodo ID3DXPRTBuffer:: ExtractTexture

Estrae i dati coefficienti da un canale colori del buffer per un intervallo di coefficienti specificato e aggiunge i dati a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Canale* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Canale di colore del buffer da cui estrarre i dati della trama.

</dd> <dt>

*StartCoefficient* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Valore iniziale del coefficiente del buffer da cui estrarre i dati della trama.

</dd> <dt>

*NumCoefficients* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di scalari, a partire da StartCoefficient, da cui estrarre i dati della trama.

</dd> <dt>

*pTexture* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un oggetto trama [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che archivia i coefficienti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
