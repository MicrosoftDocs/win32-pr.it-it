---
title: Metodo ID3DX11EffectClassInstanceVariable GetClassInstance (D3dx11effect.h)
description: Ottiene un'istanza della classe .
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Metodo GetClassInstance Direct3D 11
- Metodo GetClassInstance Interfaccia Direct3D 11, ID3DX11EffectClassInstanceVariable
- ID3DX11EffectClassInstanceVariable interface Direct3D 11 , GetClassInstance method
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0f188c1ef72b688b4c1f227bac91139b5c6cfcb2749a5f2c1fa41dd61a179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046449"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a>Metodo ID3DX11EffectClassInstanceVariable::GetClassInstance

Ottiene un'istanza della classe .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppClassInstance* 
</dt> <dd>

Tipo: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***

Puntatore a un [**puntatore ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) che verrà impostato sull'istanza della classe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

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

[ID3DX11EffectClassInstanceVariable](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





