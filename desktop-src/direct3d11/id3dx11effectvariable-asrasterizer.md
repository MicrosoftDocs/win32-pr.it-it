---
title: Metodo ID3DX11EffectVariable AsRasterizer (D3dx11effect. h)
description: Ottiene una variabile di rasterizzazione.
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- Metodo AsRasterizer Direct3D 11
- Metodo AsRasterizer Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo AsRasterizer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRasterizer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbe4edc1b1195a9d449b37897f0875b1f35aae3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996324"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a>Metodo ID3DX11EffectVariable:: AsRasterizer

Ottiene una variabile di rasterizzazione.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***

Puntatore a una variabile di rasterizzazione. Vedere [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md).

## <a name="remarks"></a>Commenti

AsRasterizer restituisce una versione della variabile Effect specializzata in una variabile di rasterizzazione. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile Effect non contiene dati di rasterizzazione.

Per verificare la validità dell'oggetto restituito, le applicazioni possono chiamare [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





