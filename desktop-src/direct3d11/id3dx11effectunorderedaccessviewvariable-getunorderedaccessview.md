---
title: Metodo ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessView (D3dx11effect.h)
description: Ottenere una visualizzazione di accesso non ordinata.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- Metodo GetUnorderedAccessView Direct3D 11
- Metodo GetUnorderedAccessView Direct3D 11, ID3DX11EffectUnorderedAccessViewVariable
- ID3DX11EffectUnorderedAccessViewVariable interface Direct3D 11, GetUnorderedAccessView method
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02ccb890d7f03a2066cb7e01633f057e821e34c74521e1bba37f9694ba72a194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676781"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a>Metodo ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessView

Ottenere una visualizzazione di accesso non ordinata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppResource* 
</dt> <dd>

Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***

Puntatore a [**un puntatore ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) che verrà impostato in fase di restituzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





