---
title: Metodo Id3DX11EffectType GetMemberTypeByName (D3dx11effect.h)
description: Ottenere un tipo di membro in base al nome.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Metodo GetMemberTypeByName Direct3D 11
- Metodo GetMemberTypeByName Interfaccia Direct3D 11, ID3DX11EffectType
- Interfaccia ID3DX11EffectType Direct3D 11, metodo GetMemberTypeByName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5988a987816ad7e5a1797d60619605228647c3dd81945b63bac9c74701bf77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460711"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a>Metodo ID3DX11EffectType::GetMemberTypeByName

Ottenere un tipo di membro in base al nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome di un membro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Puntatore a un [**oggetto ID3DX11EffectType.**](id3dx11effecttype.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

