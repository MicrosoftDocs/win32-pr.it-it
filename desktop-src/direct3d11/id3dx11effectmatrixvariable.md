---
title: Interfaccia ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Un'interfaccia della variabile di matrice accede a una matrice.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982367"
---
# <a name="id3dx11effectmatrixvariable-interface"></a>Interfaccia ID3DX11EffectMatrixVariable

Un'interfaccia della variabile di matrice accede a una matrice.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectMatrixVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectMatrixVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectMatrixVariable** dispone di questi metodi.



| Metodo                                                                                 | Descrizione                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**GetMatrix**](id3dx11effectmatrixvariable-getmatrix.md)                             | Ottenere una matrice.<br/>                                          |
| [**GetMatrixArray**](id3dx11effectmatrixvariable-getmatrixarray.md)                   | Ottenere una matrice di matrici.<br/>                              |
| [**GetMatrixTranspose**](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | Trasporre e ottenere una matrice a virgola mobile.<br/>             |
| [**GetMatrixTransposeArray**](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | Trasporre e ottenere una matrice di matrici a virgola mobile.<br/> |
| [**Sematrix**](id3dx11effectmatrixvariable-setmatrix.md)                             | Impostare una matrice a virgola mobile.<br/>                           |
| [**SetMatrixArray**](id3dx11effectmatrixvariable-setmatrixarray.md)                   | Impostare una matrice di matrici a virgola mobile.<br/>               |
| [**SetMatrixTranspose**](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | Trasponi e imposta una matrice a virgola mobile.<br/>             |
| [**SetMatrixTransposeArray**](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | Trasponi e imposta una matrice di matrici a virgola mobile.<br/> |



 

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

 

 





