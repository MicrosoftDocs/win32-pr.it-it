---
title: Interfaccia ID3DX11EffectGroup (D3dx11effect. h)
description: L'interfaccia ID3DX11EffectGroup accede a un gruppo di effetti. La durata di un oggetto ID3DX11EffectGroup è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interfaccia ID3DX11EffectGroup Direct3D 11
- Interfaccia ID3DX11EffectGroup Direct3D 11, descritta
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
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982280"
---
# <a name="id3dx11effectgroup-interface"></a>Interfaccia ID3DX11EffectGroup

L'interfaccia **ID3DX11EffectGroup** accede a un gruppo di effetti.

La durata di un oggetto **ID3DX11EffectGroup** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectGroup** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetAnnotationByIndex**](id3dx11effectgroup-getannotationbyindex.md) | Ottenere un'annotazione in base all'indice.<br/>                        |
| [**GetAnnotationByName**](id3dx11effectgroup-getannotationbyname.md)   | Ottenere un'annotazione in base al nome.<br/>                         |
| [**Getdesc**](id3dx11effectgroup-getdesc.md)                           | Ottiene una descrizione del gruppo.<br/>                          |
| [**GetTechniqueByIndex**](id3dx11effectgroup-gettechniquebyindex.md)   | Ottenere una tecnica in base all'indice.<br/>                          |
| [**GetTechniqueByName**](id3dx11effectgroup-gettechniquebyname.md)     | Ottenere una tecnica in base al nome.<br/>                           |
| [**isValid**](id3dx11effectgroup-isvalid.md)                           | Testare un effetto per verificare se contiene una sintassi valida.<br/> |



 

## <a name="remarks"></a>Commenti

Per ottenere un'interfaccia **ID3DX11EffectGroup** , chiamare un metodo come [**ID3DX11Effect:: GetGroupByName**](id3dx11effect-getgroupbyname.md).

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

 

 





