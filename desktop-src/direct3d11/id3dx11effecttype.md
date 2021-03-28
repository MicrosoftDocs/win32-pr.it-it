---
title: Interfaccia ID3DX11EffectType (D3dx11effect. h)
description: L'interfaccia ID3DX11EffectType accede alle variabili di effetto per tipo. La durata di un oggetto ID3DX11EffectType è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Interfaccia ID3DX11EffectType Direct3D 11
- Interfaccia ID3DX11EffectType Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761981"
---
# <a name="id3dx11effecttype-interface"></a>Interfaccia ID3DX11EffectType

L'interfaccia **ID3DX11EffectType** accede alle variabili di effetto per tipo.

La durata di un oggetto **ID3DX11EffectType** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectType** dispone di questi metodi.



| Metodo                                                                       | Descrizione                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [**Getdesc**](id3dx11effecttype-getdesc.md)                                 | Ottenere una descrizione del tipo di effetto.<br/>        |
| [**GetMemberName**](id3dx11effecttype-getmembername.md)                     | Ottiene il nome di un membro.<br/>              |
| [**GetMemberSemantic**](id3dx11effecttype-getmembersemantic.md)             | Ottenere la semantica collegata a un membro.<br/> |
| [**GetMemberTypeByIndex**](id3dx11effecttype-getmembertypebyindex.md)       | Ottenere un tipo di membro in base all'indice.<br/>            |
| [**GetMemberTypeByName**](id3dx11effecttype-getmembertypebyname.md)         | Ottenere un tipo di membro in base al nome.<br/>            |
| [**GetMemberTypeBySemantic**](id3dx11effecttype-getmembertypebysemantic.md) | Ottenere un tipo di membro in base alla semantica.<br/>         |
| [**isValid**](id3dx11effecttype-isvalid.md)                                 | Verifica che il tipo di effetto sia valido.<br/>   |



 

## <a name="remarks"></a>Commenti

Per ottenere informazioni su un tipo di effetto da una variabile Effect, chiamare [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





