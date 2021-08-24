---
title: Metodo ID3DX11Effect GetConstantBufferByName (D3dx11effect.h)
description: Ottenere un buffer costante in base al nome.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Metodo GetConstantBufferByName Direct3D 11
- Metodo GetConstantBufferByName Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetConstantBufferByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400be04e6955807bb6b2a60e712323f8993e55ecc031086afb3597f3962091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632561"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a>Metodo ID3DX11Effect::GetConstantBufferByName

Ottenere un buffer costante in base al nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del buffer costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Puntatore al buffer costante indicato dal nome. Vedere [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Commenti

Un effetto che contiene una variabile che verrà letta/scritta da un'applicazione richiede almeno un buffer costante. Per prestazioni ottimali, un effetto deve organizzare le variabili in uno o più buffer costanti in base alla frequenza di aggiornamento.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

