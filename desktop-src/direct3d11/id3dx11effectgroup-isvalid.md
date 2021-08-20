---
title: Metodo ID3DX11EffectGroup IsValid (D3dx11effect.h)
description: Testare un effetto per verificare se contiene una sintassi valida. | Metodo ID3DX11EffectGroup IsValid (D3dx11effect.h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- Metodo IsValid Direct3D 11
- Metodo IsValid Direct3D 11, interfaccia ID3DX11EffectGroup
- Interfaccia ID3DX11EffectGroup Direct3D 11, metodo IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28c0658c45e4091233e75c6456a9446da46a5a6d4a045bf3a533d881b42ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046249"
---
# <a name="id3dx11effectgroupisvalid-method"></a>Metodo ID3DX11EffectGroup::IsValid

Testare un effetto per verificare se contiene una sintassi valida.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** se la sintassi del codice è valida; in caso **contrario, FALSE.**

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

