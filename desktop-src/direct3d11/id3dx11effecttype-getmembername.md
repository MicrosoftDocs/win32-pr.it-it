---
title: Metodo ID3DX11EffectType GetMemberName (D3dx11effect.h)
description: Ottiene il nome di un membro.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- Metodo GetMemberName Direct3D 11
- Metodo GetMemberName Interfaccia Direct3D 11, ID3DX11EffectType
- Interfaccia ID3DX11EffectType Direct3D 11, metodo GetMemberName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db740b11e8da886d1c2b3339b1cdf64fa941dcb4947e9f399be8b49b2747bbe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532343"
---
# <a name="id3dx11effecttypegetmembername-method"></a>Metodo ID3DX11EffectType::GetMemberName

Ottiene il nome di un membro.

## <a name="syntax"></a>Sintassi


```C++
LPCSTR GetMemberName(
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

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del membro.

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

 

