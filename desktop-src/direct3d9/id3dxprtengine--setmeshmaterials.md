---
description: Imposta le proprietà del materiale mesh nella scena 3D. Usare questo metodo per specificare i parametri di dispersione sottosurface.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: Metodo ID3DXPRTEngine::SetMeshMaterials (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c24ff96b4582e86580774a1f7ac7cd889547018a5b0f138d5e43685c50e1701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293385"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>Metodo ID3DXPRTEngine::SetMeshMaterials

Imposta le proprietà del materiale mesh nella scena 3D. Usare questo metodo per specificare i parametri di dispersione sottosurface.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppMaterials* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

Indirizzo di un puntatore alle proprietà del materiale della mesh desiderate. Vedere [**D3DXSHMATERIAL**](d3dxshmaterial.md).

</dd> <dt>

*NumMeshes* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice della mesh su cui impostare le proprietà del materiale.

</dd> <dt>

*NumChannels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di canali di colore da impostare nella mesh. Impostare su 1 per specificare materiali grigi (R = G = B) o 3 per abilitare gli effetti di colorazione. Se si intende modificare questo parametro, impostare prima l'oggetto albedo usando un altro metodo, ad esempio [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) o [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).

</dd> <dt>

*bSetAlbedo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE,** imposta l'albedo della mesh su ppMaterials, sovrascrivendo tutti i valori texel e vertex albedo esistenti. Se **FALSE,** mantiene tutti i valori texel e vertex albedo esistenti impostati da altri metodi; NumChannels deve corrispondere al parametro NumChannels usato per creare il buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex.**](d3dxcreateprtbuffertex.md)

</dd> <dt>

*fLengthScale* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Scala della scena 3D rispetto a un cubo di 1 mm. Usato per i calcoli di dispersione sottosurface.

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

 

 
