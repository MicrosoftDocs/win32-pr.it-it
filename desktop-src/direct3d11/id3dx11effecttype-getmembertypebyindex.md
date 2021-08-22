---
title: Metodo ID3DX11EffectType GetMemberTypeByIndex (D3dx11effect.h)
description: Ottiene un tipo di membro in base all'indice.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- Metodo GetMemberTypeByIndex Direct3D 11
- Metodo GetMemberTypeByIndex Interfaccia Direct3D 11, ID3DX11EffectType
- Id3DX11EffectType interface Direct3D 11 , GetMemberTypeByIndex method
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53500ec94791ff534bf6b3c9a2e7d46a51b7b69bc889f35515e9b653c5bbb422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532323"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a>Metodo ID3DX11EffectType::GetMemberTypeByIndex

Ottiene un tipo di membro in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Puntatore a [**id3DX11EffectType.**](id3dx11effecttype.md)

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

