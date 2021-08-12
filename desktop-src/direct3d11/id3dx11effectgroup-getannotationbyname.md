---
title: Metodo ID3DX11EffectGroup GetAnnotationByName (D3dx11effect.h)
description: Ottiene un'annotazione in base al nome. | Metodo ID3DX11EffectGroup GetAnnotationByName (D3dx11effect.h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Metodo GetAnnotationByName Direct3D 11
- Metodo GetAnnotationByName Direct3D 11, interfaccia ID3DX11EffectGroup
- Id3DX11EffectGroup interface Direct3D 11 , GetAnnotationByName method
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d80c0d59a1fd0a58c756d72f6215f13b4e3391e44828aa8e1bcff23063292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535740"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a>Metodo ID3DX11EffectGroup::GetAnnotationByName

Ottiene un'annotazione in base al nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome dell'elemento Annotation.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a [**id3DX11EffectVariable.**](id3dx11effectvariable.md) Si noti che se l'annotazione non viene trovata, **id3DX11EffectVariable** restituito sarà vuoto. È necessario chiamare il metodo [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) per determinare se l'annotazione è stata trovata.

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

 

