---
title: Metodo ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect.h)
description: Ottiene un'annotazione in base al nome. | Metodo ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect.h)
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- Metodo GetAnnotationByName Direct3D 11
- Metodo GetAnnotationByName Direct3D 11, interfaccia ID3DX11EffectTechnique
- ID3DX11EffectTechnique interface Direct3D 11 , GetAnnotationByName method
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ba87c400129d9caab88657f0d554c67a75072feaf425054ee638ccf7b3d11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069661"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a>Metodo ID3DX11EffectTechnique::GetAnnotationByName

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

Nome dell'annotazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a [**id3DX11EffectVariable.**](id3dx11effectvariable.md)

## <a name="remarks"></a>Commenti

Usare un'annotazione per associare una parte di metadati a una tecnica.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

