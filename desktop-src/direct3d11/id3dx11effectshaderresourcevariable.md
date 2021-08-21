---
title: Interfaccia ID3DX11EffectShaderResourceVariable (D3dx11effect.h)
description: Un'interfaccia shader-risorsa accede a una risorsa shader.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- INTERFACCIA ID3DX11EffectShaderResourceVariable Direct3D 11
- ID3DX11EffectShaderResourceVariable interface Direct3D 11 , descritto
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1cdfce3ce5fe907de5b0149f2280d8b1e34a8761c56cf9e83e316ea253d7366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533287"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a>Interfaccia ID3DX11EffectShaderResourceVariable

Un'interfaccia shader-risorsa accede a una risorsa shader.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11EffectShaderResourceVariable** eredita da [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectShaderResourceVariable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectShaderResourceVariable** include questi metodi.



| Metodo                                                                           | Descrizione                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [**GetResource**](id3dx11effectshaderresourcevariable-getresource.md)           | Ottenere una risorsa shader.<br/>            |
| [**GetResourceArray**](id3dx11effectshaderresourcevariable-getresourcearray.md) | Ottenere una matrice di risorse shader.<br/> |
| [**SetResource**](id3dx11effectshaderresourcevariable-setresource.md)           | Impostare una risorsa shader.<br/>            |
| [**SetResourceArray**](id3dx11effectshaderresourcevariable-setresourcearray.md) | Impostare una matrice di risorse shader.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce di Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





