---
title: Interfaccia ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Un'interfaccia shader-Resource accede a una risorsa shader.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Interfaccia ID3DX11EffectShaderResourceVariable Direct3D 11
- Interfaccia ID3DX11EffectShaderResourceVariable Direct3D 11, descritta
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
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996297"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a>Interfaccia ID3DX11EffectShaderResourceVariable

Un'interfaccia shader-Resource accede a una risorsa shader.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectShaderResourceVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderResourceVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectShaderResourceVariable** dispone di questi metodi.



| Metodo                                                                           | Descrizione                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [**GetResource**](id3dx11effectshaderresourcevariable-getresource.md)           | Ottenere una risorsa shader.<br/>            |
| [**GetResourceArray**](id3dx11effectshaderresourcevariable-getresourcearray.md) | Ottenere una matrice di risorse dello shader.<br/> |
| [**SetResource**](id3dx11effectshaderresourcevariable-setresource.md)           | Impostare una risorsa shader.<br/>            |
| [**SetResourceArray**](id3dx11effectshaderresourcevariable-setresourcearray.md) | Impostare una matrice di risorse dello shader.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





