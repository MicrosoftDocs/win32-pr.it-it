---
title: Interfaccia ID3DX11EffectUnorderedAccessViewVariable (D3dx11effect. h)
description: Accede a una visualizzazione di accesso non ordinato.
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- Interfaccia ID3DX11EffectUnorderedAccessViewVariable Direct3D 11
- Interfaccia ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48161ad4d9fc1773889fab0e8a0fd9a21ec793e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995804"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a>Interfaccia ID3DX11EffectUnorderedAccessViewVariable

Accede a una visualizzazione di accesso non ordinato.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectUnorderedAccessViewVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectUnorderedAccessViewVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectUnorderedAccessViewVariable** dispone di questi metodi.



| Metodo                                                                                                      | Descrizione                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetUnorderedAccessView**](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | Ottenere una visualizzazione di accesso non ordinato.<br/>           |
| [**GetUnorderedAccessViewArray**](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | Ottenere una matrice di viste con accesso non ordinato.<br/> |
| [**SetUnorderedAccessView**](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | Impostare una visualizzazione di accesso non ordinato.<br/>           |
| [**SetUnorderedAccessViewArray**](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | Impostare una matrice di viste con accesso non ordinato.<br/> |



 

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

 

 





