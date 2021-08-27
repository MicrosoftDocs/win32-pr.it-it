---
title: Metodo ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect.h)
description: Ottiene un'annotazione in base all'indice. | Metodo ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect.h)
ms.assetid: 703663b0-ee00-4686-a038-6c99ce61266b
keywords:
- Metodo GetAnnotationByIndex Direct3D 11
- Metodo GetAnnotationByIndex Direct3D 11, INTERFACCIA ID3DX11EffectTechnique
- ID3DX11EffectTechnique interface Direct3D 11 , Metodo GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7de800e05dfb6731340ad7255019d4017eefb0cc88f9069e8c4aae4f327071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532569"
---
# <a name="id3dx11effecttechniquegetannotationbyindex-method"></a>Metodo ID3DX11EffectTechnique::GetAnnotationByIndex

Ottiene un'annotazione in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero del puntatore a interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a un [**oggetto ID3DX11EffectVariable.**](id3dx11effectvariable.md)

## <a name="remarks"></a>Commenti

Usare un'annotazione per associare una parte di metadati a una tecnica.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

