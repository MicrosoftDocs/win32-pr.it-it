---
description: Controlla i parametri di creazione della trama.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Funzione D3DXCheckTextureRequirements (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c7166f981c0351054a2a6c359127a4ce1959b45a6e71c44db9e2546825bc5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496101"
---
# <a name="d3dxchecktexturerequirements-function"></a>Funzione D3DXCheckTextureRequirements

Controlla i parametri di creazione della trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*pWidth* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore alla larghezza richiesta in pixel o **NULL.** Restituisce le dimensioni corrette.

</dd> <dt>

*pHeight* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore all'altezza richiesta in pixel o **NULL.** Restituisce le dimensioni corrette.

</dd> <dt>

*pNumMipLevels* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore al numero di livelli mipmap richiesti o **NULL.** Restituisce il numero corretto di livelli mipmap.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 o [**D3DUSAGE \_ RENDERTARGET.**](d3dusage.md) L'impostazione di questo flag su D3DUSAGE RENDERTARGET indica che la \_ superficie deve essere usata come destinazione di rendering. La risorsa può quindi essere passata al parametro pNewRenderTarget del [**metodo SetRenderTarget.**](/windows/desktop/api) Se **si specifica D3DUSAGE \_ RENDERTARGET,** l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

</dd> <dt>

*pFormat* \[ in, out\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)\***

Puntatore a un membro del [tipo enumerato D3DFORMAT.](d3dformat.md) Specifica il formato pixel desiderato o **NULL.** Restituisce il formato corretto.

</dd> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del tipo [**enumerato D3DPOOL,**](./d3dpool.md) che descrive la classe di memoria in cui deve essere inserita la trama.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.

## <a name="remarks"></a>Commenti

Se i parametri di questa funzione non sono validi, questa funzione restituisce i parametri corretti.

Questa funzione usa l'euristica seguente per confrontare i requisiti richiesti con i formati disponibili:

-   Non scegliere un formato con meno canali.
-   Evitare [i formati FOURCC](d3dformat.md) e a 24 bit a meno che non siano richiesti in modo esplicito.
-   Provare a non aggiungere nuovi canali.
-   Provare a non modificare il numero di bit per canale.
-   Provare a evitare la conversione tra tipi di formati. Ad esempio, evitare di convertire un formato ARGB in un formato di profondità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
