---
title: Metodo ID3DX11EffectVariable GetMemberByIndex (D3dx11effect.h)
description: Ottenere un membro della struttura in base all'indice.
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- Metodo GetMemberByIndex Direct3D 11
- Metodo GetMemberByIndex Direct3D 11, interfaccia ID3DX11EffectVariable
- Id3DX11EffectVariable interface Direct3D 11, GetMemberByIndex method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5176eb220dc928a98ec0f579afaeab1c81b1a7ff9ef3555736ed471bf15b9117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124496"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a>Metodo ID3DX11EffectVariable::GetMemberByIndex

Ottenere un membro della struttura in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetMemberByIndex(
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

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a un [**oggetto ID3DX11EffectVariable.**](id3dx11effectvariable.md)

## <a name="remarks"></a>Commenti

Se la variabile effect è una struttura , usare questo metodo per cercare un membro in base all'indice.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

