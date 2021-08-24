---
title: Metodo ID3DX11Effect GetConstantBufferByIndex (D3dx11effect.h)
description: Ottiene un buffer costante in base all'indice.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Metodo GetConstantBufferByIndex Direct3D 11
- Metodo GetConstantBufferByIndex Direct3D 11, interfaccia ID3DX11Effect
- ID3DX11Effect interface Direct3D 11 , GetConstantBufferByIndex method
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d2ce34bb6bde85600e57182151e8c270885e60f919f22a723228b14dd17927a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632601"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a>Metodo ID3DX11Effect::GetConstantBufferByIndex

Ottiene un buffer costante in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
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

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Puntatore a [**id3DX11EffectConstantBuffer.**](id3dx11effectconstantbuffer.md)

## <a name="remarks"></a>Commenti

Un effetto che contiene una variabile che verrà letta/scritta da un'applicazione richiede almeno un buffer costante. Per ottenere prestazioni ottimali, un effetto dovrebbe organizzare le variabili in uno o più buffer costanti in base alla frequenza di aggiornamento.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

