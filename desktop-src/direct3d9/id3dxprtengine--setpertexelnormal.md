---
description: Imposta un vettore normale per ogni texel in un oggetto trama. Questo metodo viene usato per archiviare vettori normali dei vertici da una mesh (o normali dei vertici interpolate se viene calcolato il trasferimento della radia precompilazione basato su pixel).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: Metodo ID3DXPRTEngine::SetPerTexelNormal (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75877e8af86a22f80703742f148d5171e3a99e5c0c580bff588c27deba269b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293375"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>Metodo ID3DXPRTEngine::SetPerTexelNormal

Imposta un vettore normale per ogni texel in un oggetto trama. Questo metodo viene usato per archiviare vettori normali dei vertici da una mesh (o normali dei vertici interpolate se viene calcolato il trasferimento della radia precompilazione basato su pixel).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNormalTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un oggetto trama [**IDirect3DTexture9**](/windows/desktop/api) che funge da mappa normale dello spazio oggetto in cui archiviare i vettori normali. La trama deve avere le stesse dimensioni di [**ID3DXPRTBuffer**](id3dxprtbuffer.md) e deve essere in grado di archiviare formati di trama firmati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
