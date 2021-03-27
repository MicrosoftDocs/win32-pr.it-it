---
title: Metodo GetMemberName di ID3DX11EffectType (D3dx11effect. h)
description: Ottiene il nome di un membro.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- Metodo GetMemberName Direct3D 11
- Metodo GetMemberName Direct3D 11, interfaccia ID3DX11EffectType
- Interfaccia ID3DX11EffectType Direct3D 11, Metodo GetMemberName
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
ms.openlocfilehash: a4aa9a24067d8ef19680ca58e41659da850659b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355169"
---
# <a name="id3dx11effecttypegetmembername-method"></a>Metodo ID3DX11EffectType:: GetMemberName

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del membro.

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

