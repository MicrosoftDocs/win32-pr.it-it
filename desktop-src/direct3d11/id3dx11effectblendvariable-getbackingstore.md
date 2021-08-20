---
title: Metodo GETBackingStore ID3DX11EffectBlendVariable (D3dx11effect.h)
description: Ottenere un puntatore a una variabile di stato di blend.
ms.assetid: 809daaad-9bf0-48fb-ae91-f237c43db324
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Direct3D 11, interfaccia ID3DX11EffectBlendVariable
- INTERFACCIA ID3DX11EffectBlendVariable Direct3D 11, metodo GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f02f09c0db4ec56ee592dc39ddbb7fef1ae52d328edec5d9a5c9fd17b769ef58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046559"
---
# <a name="id3dx11effectblendvariablegetbackingstore-method"></a>Metodo ID3DX11EffectBlendVariable::GetBackingStore

Ottenere un puntatore a una variabile di stato di blend.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBackingStore(
   UINT             Index,
   D3D11_BLEND_DESC *pBlendDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di descrizioni dello stato di blend. Se nell'effetto è presente una sola variabile di stato di blend, usare 0.

</dd> <dt>

*pBlendDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***

Puntatore a una descrizione dello stato di blend (vedere [**D3D11 \_ BLEND \_ DESC).**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Le variabili degli effetti vengono salvate in memoria nell'archivio di backup. Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo. I dati dell'archivio di backup possono essere usati per ricreare la variabile quando necessario.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

