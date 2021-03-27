---
title: Metodo ID3DX11EffectVariable AsString (D3dx11effect. h)
description: Ottiene una variabile di stringa.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- Metodo AsString Direct3D 11
- Metodo AsString Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, Metodo AsString
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73092dcd27b5651ad6205fa05bcbb13cc1f86116
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356144"
---
# <a name="id3dx11effectvariableasstring-method"></a>Metodo ID3DX11EffectVariable:: AsString

Ottiene una variabile di stringa.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***

Puntatore a una variabile di stringa. Vedere [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).

## <a name="remarks"></a>Commenti

AsString restituisce una versione della variabile Effect specializzata in una variabile di stringa. Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile Effect non contiene dati di tipo stringa.

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

 

 





