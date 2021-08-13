---
title: Interfaccia ID3DX11EffectGroup (D3dx11effect.h)
description: L'interfaccia ID3DX11EffectGroup accede a un gruppo Effect. La durata di un oggetto ID3DX11EffectGroup è uguale alla durata dell'oggetto ID3DX11Effect padre.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interfaccia ID3DX11EffectGroup Direct3D 11
- Interfaccia ID3DX11EffectGroup Direct3D 11 , descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa42a884be0abd15f0d16403a95d859d89cd472fc630b51ffe586e703e1a8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046229"
---
# <a name="id3dx11effectgroup-interface"></a>Interfaccia ID3DX11EffectGroup

**L'interfaccia ID3DX11EffectGroup** accede a un gruppo Effect.

La durata di un **oggetto ID3DX11EffectGroup** è uguale alla durata dell'oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectGroup** include questi metodi.



| Metodo                                                                  | Descrizione                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetAnnotationByIndex**](id3dx11effectgroup-getannotationbyindex.md) | Ottiene un'annotazione in base all'indice.<br/>                        |
| [**GetAnnotationByName**](id3dx11effectgroup-getannotationbyname.md)   | Ottiene un'annotazione in base al nome.<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | Ottiene una descrizione del gruppo.<br/>                          |
| [**GetTechniqueByIndex**](id3dx11effectgroup-gettechniquebyindex.md)   | Ottenere una tecnica in base all'indice.<br/>                          |
| [**GetTechniqueByName**](id3dx11effectgroup-gettechniquebyname.md)     | Ottenere una tecnica in base al nome.<br/>                           |
| [**isValid**](id3dx11effectgroup-isvalid.md)                           | Testare un effetto per verificare se contiene una sintassi valida.<br/> |



 

## <a name="remarks"></a>Commenti

Per ottenere **un'interfaccia ID3DX11EffectGroup,** chiamare un metodo come [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce effetti 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





