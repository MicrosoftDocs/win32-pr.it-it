---
title: Interfaccia ID3DX11EffectMatrixVariable (D3dx11effect.h)
description: Un'interfaccia matrice-variabile accede a una matrice.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Id3DX11EffectMatrixVariable interface Direct3D 11
- ID3DX11EffectMatrixVariable interface Direct3D 11 , descritto
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
ms.openlocfilehash: e9daff97a1980c7f1e5647c0e436d5e774a7a7b575b3100f1164af8b97010dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535087"
---
# <a name="id3dx11effectmatrixvariable-interface"></a>Interfaccia ID3DX11EffectMatrixVariable

Un'interfaccia matrice-variabile accede a una matrice.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11EffectMatrixVariable** eredita da [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectMatrixVariable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **ID3DX11EffectMatrixVariable.**



| Metodo                                                                                 | Descrizione                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**GetMatrix**](id3dx11effectmatrixvariable-getmatrix.md)                             | Ottenere una matrice.<br/>                                          |
| [**GetMatrixArray**](id3dx11effectmatrixvariable-getmatrixarray.md)                   | Ottiene una matrice di matrici.<br/>                              |
| [**GetMatrixTranspose**](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | Trasporre e ottenere una matrice a virgola mobile.<br/>             |
| [**GetMatrixTransposeArray**](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | Trasporre e ottenere una matrice di matrici a virgola mobile.<br/> |
| [**SetMatrix**](id3dx11effectmatrixvariable-setmatrix.md)                             | Impostare una matrice a virgola mobile.<br/>                           |
| [**SetMatrixArray**](id3dx11effectmatrixvariable-setmatrixarray.md)                   | Impostare una matrice di matrici a virgola mobile.<br/>               |
| [**SetMatrixTranspose**](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | Trasporre e impostare una matrice a virgola mobile.<br/>             |
| [**SetMatrixTransposeArray**](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | Trasporre e impostare una matrice di matrici a virgola mobile.<br/> |



 

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

 

 





