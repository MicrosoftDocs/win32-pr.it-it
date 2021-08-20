---
title: Metodo ID3DX11EffectGroup GetTechniqueByName (D3dx11effect.h)
description: Ottenere una tecnica in base al nome. | Metodo ID3DX11EffectGroup GetTechniqueByName (D3dx11effect.h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Metodo GetTechniqueByName Direct3D 11
- Metodo GetTechniqueByName Direct3D 11, interfaccia ID3DX11EffectGroup
- Id3DX11EffectGroup interface Direct3D 11 , GetTechniqueByName method
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590defa7477ad41d1e861dc7a8afa05370f4d83d7846c99fa1086aae94c57c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046259"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a>Metodo ID3DX11EffectGroup::GetTechniqueByName

Ottenere una tecnica in base al nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome della tecnica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Puntatore a [**id3DX11EffectTechnique**](id3dx11effecttechnique.md)o **NULL** se la tecnica non viene trovata.

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

