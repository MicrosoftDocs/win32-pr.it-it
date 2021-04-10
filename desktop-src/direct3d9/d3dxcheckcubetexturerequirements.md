---
description: Verifica i parametri di creazione della trama del cubo.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: Funzione D3DXCheckCubeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762352"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a>D3DXCheckCubeTextureRequirements (funzione)

Verifica i parametri di creazione della trama del cubo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.

</dd> <dt>

*psize* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore alla larghezza e all'altezza richieste in pixel o **null**. Restituisce la dimensione corretta.

</dd> <dt>

*pNumMipLevels* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore al numero di livelli di mipmap richiesti o **null**. Restituisce il numero corretto di livelli di mipmap.

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 o D3DUSAGE \_ RENDERTARGET. L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering. La risorsa può quindi essere passata al parametro pNewRenderTarget del metodo [**SetRenderTarget**](/windows/desktop/api) . Se \_ viene specificato D3DUSAGE RENDERTARGET, l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

</dd> <dt>

*pFormat* \[ in uscita\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)\***

Puntatore a un membro del tipo enumerato [D3DFORMAT](d3dformat.md) . Specifica il formato pixel desiderato o **null**. Restituisce il formato corretto.

</dd> <dt>

*Pool* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Se i parametri di questa funzione non sono validi, questa funzione restituisce parametri corretti.

Le trame del cubo differiscono dalle altre superfici perché sono raccolte di superfici. Per chiamare [**SetRenderTarget**](/windows/desktop/api) con una trama del cubo, è necessario selezionare un singolo volto usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passare la superficie risultante a **SetRenderTarget**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
