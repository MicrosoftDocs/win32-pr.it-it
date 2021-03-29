---
title: Metodo ID3DX11EffectConstantBuffer SetConstantBuffer (D3dx11effect. h)
description: Impostare un buffer di costanti.
ms.assetid: 288e029a-e69a-4f58-be3f-8f9900c0e1dd
keywords:
- Metodo SetConstantBuffer Direct3D 11
- Metodo SetConstantBuffer Direct3D 11, interfaccia ID3DX11EffectConstantBuffer
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, metodo SetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12249d9830ced43c3a56a2c8cf51942e66f6494e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235175"
---
# <a name="id3dx11effectconstantbuffersetconstantbuffer-method"></a>Metodo ID3DX11EffectConstantBuffer:: SetConstantBuffer

Impostare un buffer di costanti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConstantBuffer(
   ID3D11Buffer *pConstantBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pConstantBuffer* 
</dt> <dd>

Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***

Puntatore a un'interfaccia del buffer costante. Vedere [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).

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

 

 





