---
title: Interfaccia ID3DX11EffectVectorVariable (D3dx11effect. h)
description: Un'interfaccia a variabili di vettore accede a un vettore a quattro componenti.
ms.assetid: 191d373b-0562-4d7b-ac3f-cd24abf259bc
keywords:
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9235a4047617dd2e5ff9f14925908ae7a0dc1060
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995780"
---
# <a name="id3dx11effectvectorvariable-interface"></a>Interfaccia ID3DX11EffectVectorVariable

Un'interfaccia a variabili di vettore accede a un vettore a quattro componenti.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectVectorVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectVectorVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectVectorVariable** dispone di questi metodi.



| Metodo                                                                         | Descrizione                                                                         |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**GetBoolVector**](id3dx11effectvectorvariable-getboolvector.md)             | Ottenere un vettore a quattro componenti contenente dati booleani.<br/>                  |
| [**GetBoolVectorArray**](id3dx11effectvectorvariable-getboolvectorarray.md)   | Ottenere una matrice di vettori a quattro componenti che contengono dati booleani.<br/>        |
| [**GetFloatVector**](id3dx11effectvectorvariable-getfloatvector.md)           | Ottenere un vettore a quattro componenti che contiene dati a virgola mobile.<br/>           |
| [**GetFloatVectorArray**](id3dx11effectvectorvariable-getfloatvectorarray.md) | Ottenere una matrice di vettori a quattro componenti che contengono dati a virgola mobile.<br/> |
| [**GetIntVector**](id3dx11effectvectorvariable-getintvector.md)               | Ottenere un vettore a quattro componenti contenente dati Integer.<br/>                  |
| [**GetIntVectorArray**](id3dx11effectvectorvariable-getintvectorarray.md)     | Ottenere una matrice di vettori a quattro componenti che contengono dati di tipo Integer.<br/>        |
| [**SetBoolVector**](id3dx11effectvectorvariable-setboolvector.md)             | Impostare un vettore a quattro componenti contenente dati booleani.<br/>                  |
| [**SetBoolVectorArray**](id3dx11effectvectorvariable-setboolvectorarray.md)   | Impostare una matrice di vettori a quattro componenti che contengono dati booleani.<br/>        |
| [**SetFloatVector**](id3dx11effectvectorvariable-setfloatvector.md)           | Impostare un vettore a quattro componenti che contiene dati a virgola mobile.<br/>           |
| [**SetFloatVectorArray**](id3dx11effectvectorvariable-setfloatvectorarray.md) | Impostare una matrice di vettori a quattro componenti che contengono dati a virgola mobile.<br/> |
| [**SetIntVector**](id3dx11effectvectorvariable-setintvector.md)               | Impostare un vettore a quattro componenti contenente dati Integer.<br/>                  |
| [**SetIntVectorArray**](id3dx11effectvectorvariable-setintvectorarray.md)     | Impostare una matrice di vettori a quattro componenti che contengono dati di tipo Integer.<br/>        |



 

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

 

 





