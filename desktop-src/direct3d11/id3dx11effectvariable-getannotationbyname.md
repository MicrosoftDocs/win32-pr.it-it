---
title: Metodo ID3DX11EffectVariable GetAnnotationByName (D3dx11effect.h)
description: Ottenere un'annotazione in base al nome. | Metodo ID3DX11EffectVariable GetAnnotationByName (D3dx11effect.h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Metodo GetAnnotationByName Direct3D 11
- Metodo GetAnnotationByName Direct3D 11, interfaccia ID3DX11EffectVariable
- Id3DX11EffectVariable interface Direct3D 11, GetAnnotationByName method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766366497187fec9c6dab3c5f92f5fbca23f5729297976d2c9e2c7e4ffb0deef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119376461"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a>Metodo ID3DX11EffectVariable::GetAnnotationByName

Ottenere un'annotazione in base al nome.

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

Puntatore a un [**oggetto ID3DX11EffectVariable.**](id3dx11effectvariable.md) Si noti che se l'annotazione non viene trovata, **id3DX11EffectVariable** restituito sarà vuoto. Il [**metodo ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) deve essere chiamato per determinare se l'annotazione è stata trovata.

## <a name="remarks"></a>Commenti

Le annonazioni possono essere associate a una tecnica, a un passaggio o a una variabile globale.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

