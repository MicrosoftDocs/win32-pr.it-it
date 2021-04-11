---
description: Verifica i parametri per la creazione di trame.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Funzione D3DXCheckTextureRequirements (D3dx9tex. h)
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
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235062"
---
# <a name="d3dxchecktexturerequirements-function"></a>D3DXCheckTextureRequirements (funzione)

Verifica i parametri per la creazione di trame.

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

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*pWidth* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore alla larghezza richiesta, in pixel, o **null**. Restituisce la dimensione corretta.

</dd> <dt>

*pHeight* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore all'altezza richiesta, in pixel, o **null**. Restituisce la dimensione corretta.

</dd> <dt>

*pNumMipLevels* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore al numero di livelli di mipmap richiesti o **null**. Restituisce il numero corretto di livelli di mipmap.

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 o [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering. La risorsa può quindi essere passata al parametro pNewRenderTarget del metodo [**SetRenderTarget**](/windows/desktop/api) . Se viene specificato **D3DUSAGE \_ RENDERTARGET** , l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).

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

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.

## <a name="remarks"></a>Commenti

Se i parametri di questa funzione non sono validi, questa funzione restituisce parametri corretti.

Questa funzione usa l'euristica seguente quando si confrontano i requisiti richiesti rispetto ai formati disponibili:

-   Non scegliere un formato con un minor numero di canali.
-   Evitare i formati [fourcc](d3dformat.md) e a 24 bit a meno che non vengano richiesti in modo esplicito.
-   Provare a non aggiungere nuovi canali.
-   Provare a non modificare il numero di bit per canale.
-   Provare a evitare la conversione tra tipi di formati. Ad esempio, evitare di convertire un formato ARGB in un formato di profondità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
