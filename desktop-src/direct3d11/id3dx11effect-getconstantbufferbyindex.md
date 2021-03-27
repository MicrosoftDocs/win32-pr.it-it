---
title: Metodo ID3DX11Effect GetConstantBufferByIndex (D3dx11effect. h)
description: Ottenere un buffer costante in base all'indice.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Metodo GetConstantBufferByIndex Direct3D 11
- Metodo GetConstantBufferByIndex Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetConstantBufferByIndex
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
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982424"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a>Metodo ID3DX11Effect:: GetConstantBufferByIndex

Ottenere un buffer costante in base all'indice.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Puntatore a un [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Commenti

Un effetto che contiene una variabile che verrà letta/scritta da un'applicazione richiede almeno un buffer costante. Per ottenere prestazioni ottimali, un effetto dovrebbe organizzare le variabili in uno o più buffer costanti in base alla relativa frequenza di aggiornamento.

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

