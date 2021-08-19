---
title: Metodo ID3DX11EffectVariable GetMemberByName (D3dx11effect.h)
description: Ottiene un membro della struttura in base al nome.
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- Metodo GetMemberByName Direct3D 11
- Metodo GetMemberByName Direct3D 11, interfaccia ID3DX11EffectVariable
- ID3DX11EffectVariable interface Direct3D 11 , GetMemberByName method
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84aed91fd3bb2b735de08a002f924bab1bcc8f5f279a4a6047de2b7b73cd7844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734253"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a>Metodo ID3DX11EffectVariable::GetMemberByName

Ottiene un membro della struttura in base al nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del membro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a [**id3DX11EffectVariable.**](id3dx11effectvariable.md)

## <a name="remarks"></a>Commenti

Se la variabile dell'effetto è una struttura, usare questo metodo per cercare un membro in base al nome.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

