---
title: Metodo ID3DX11EffectVariable AsRenderTargetView (D3dx11effect. h)
description: Ottenere una variabile di visualizzazione della destinazione di rendering.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- Metodo AsRenderTargetView Direct3D 11
- Metodo AsRenderTargetView Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo AsRenderTargetView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca6270503ff786b3f4a319e3f068ba76acada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996321"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a>Metodo ID3DX11EffectVariable:: AsRenderTargetView

Ottenere una variabile di visualizzazione della destinazione di rendering.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***

Puntatore a una variabile di visualizzazione della destinazione di rendering. Vedere [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).

## <a name="remarks"></a>Commenti

Questo metodo restituisce una versione della variabile di effetto che è stata specializzata in una variabile di visualizzazione della destinazione di rendering. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile Effect non contiene dati di visualizzazione della destinazione di rendering.

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

 

 





