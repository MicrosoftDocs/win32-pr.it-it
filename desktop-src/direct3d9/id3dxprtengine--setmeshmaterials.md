---
description: Imposta le proprietà del materiale mesh nella scena 3D. Utilizzare questo metodo per specificare i parametri di dispersione della sottosuperficie.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'Metodo ID3DXPRTEngine:: SetMeshMaterials (D3DX9Mesh. h)'
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
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355684"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>Metodo ID3DXPRTEngine:: SetMeshMaterials

Imposta le proprietà del materiale mesh nella scena 3D. Utilizzare questo metodo per specificare i parametri di dispersione della sottosuperficie.

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

*ppMaterials* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

Indirizzo di un puntatore alle proprietà del materiale mesh desiderato. Vedere [**D3DXSHMATERIAL**](d3dxshmaterial.md).

</dd> <dt>

*NumMeshes* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice della mesh in cui impostare le proprietà del materiale.

</dd> <dt>

*NumChannels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di canali dei colori da impostare nella rete. Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore. Se si intende modificare questo parametro, impostare prima di tutto l'albedo usando un altro metodo, ad esempio [**ID3DXPRTEngine:: SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) o [**ID3DXPRTEngine:: SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).

</dd> <dt>

*bSetAlbedo* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **true**, imposta l'albedo della mesh su ppMaterials, sovrascrivendo tutti i valori dell'albedo di Texel e vertex esistenti. Se **false**, conserva tutti i valori dell'albedo di Texel e vertex esistenti impostati da altri metodi; NumChannels deve corrispondere al parametro NumChannels usato per creare il buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).

</dd> <dt>

*fLengthScale* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Scala della scena 3D rispetto a un cubo da 1 mm. Utilizzato per i calcoli di dispersione della sottosuperficie.

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

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
