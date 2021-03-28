---
title: Metodo ID3DX11EffectConstantBuffer GetConstantBuffer (D3dx11effect. h)
description: Ottenere un buffer costante.
ms.assetid: 857b3dc2-41ae-4a52-904a-9ca8f0afeb9e
keywords:
- Metodo GetConstantBuffer Direct3D 11
- Metodo GetConstantBuffer Direct3D 11, interfaccia ID3DX11EffectConstantBuffer
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, metodo GetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041ca2fea028cb86d0959313bae73c320e6e5a36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058693"
---
# <a name="id3dx11effectconstantbuffergetconstantbuffer-method"></a>Metodo ID3DX11EffectConstantBuffer:: GetConstantBuffer

Ottenere un buffer costante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConstantBuffer(
   ID3D11Buffer **ppConstantBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppConstantBuffer* 
</dt> <dd>

Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***

Indirizzo di un puntatore a un'interfaccia del buffer costante. Vedere [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

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

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





