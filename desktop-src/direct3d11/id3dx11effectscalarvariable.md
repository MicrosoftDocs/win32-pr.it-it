---
title: Interfaccia ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Un'interfaccia con variabile effetto-scalare accede ai valori scalari.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- Interfaccia ID3DX11EffectScalarVariable Direct3D 11
- Interfaccia ID3DX11EffectScalarVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234950"
---
# <a name="id3dx11effectscalarvariable-interface"></a>Interfaccia ID3DX11EffectScalarVariable

Un'interfaccia con variabile effetto-scalare accede ai valori scalari.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectScalarVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectScalarVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectScalarVariable** dispone di questi metodi.



| Metodo                                                             | Descrizione                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBool**](id3dx11effectscalarvariable-getbool.md)             | Ottenere una variabile booleana.<br/>                   |
| [**GetBoolArray**](id3dx11effectscalarvariable-getboolarray.md)   | Ottenere una matrice di variabili booleane.<br/>        |
| [**GetFloat**](id3dx11effectscalarvariable-getfloat.md)           | Ottenere una variabile a virgola mobile.<br/>            |
| [**GetFloatArray**](id3dx11effectscalarvariable-getfloatarray.md) | Ottenere una matrice di variabili a virgola mobile.<br/> |
| [**GetInt**](id3dx11effectscalarvariable-getint.md)               | Ottiene una variabile di tipo Integer.<br/>                  |
| [**GetIntArray**](id3dx11effectscalarvariable-getintarray.md)     | Ottenere una matrice di variabili Integer.<br/>        |
| [**DiBOOL**](id3dx11effectscalarvariable-setbool.md)             | Impostare una variabile booleana.<br/>                   |
| [**SetBoolArray**](id3dx11effectscalarvariable-setboolarray.md)   | Impostare una matrice di variabili booleane.<br/>        |
| [**SetFloat**](id3dx11effectscalarvariable-setfloat.md)           | Impostare una variabile a virgola mobile.<br/>            |
| [**SetFloatArray**](id3dx11effectscalarvariable-setfloatarray.md) | Impostare una matrice di variabili a virgola mobile.<br/> |
| [**SetInt**](id3dx11effectscalarvariable-setint.md)               | Impostare una variabile integer.<br/>                  |
| [**SetIntArray**](id3dx11effectscalarvariable-setintarray.md)     | Impostare una matrice di variabili Integer.<br/>        |



 

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

 

 





