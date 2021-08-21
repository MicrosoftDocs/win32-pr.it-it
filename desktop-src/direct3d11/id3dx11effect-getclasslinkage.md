---
title: Metodo ID3DX11Effect GetClassLinkage (D3dx11effect.h)
description: Ottiene un'interfaccia di collegamento della classe.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- Metodo GetClassLinkage Direct3D 11
- Metodo GetClassLinkage Direct3D 11, interfaccia ID3DX11Effect
- INTERFACCIA ID3DX11Effect Direct3D 11, metodo GetClassLinkage
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f4a34ad8ff2e53d521d4fd7a1510332dddf8ff7197eac17bf4231a26e98f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632661"
---
# <a name="id3dx11effectgetclasslinkage-method"></a>Metodo ID3DX11Effect::GetClassLinkage

Ottiene un'interfaccia di collegamento della classe.

## <a name="syntax"></a>Sintassi


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***

Restituisce un puntatore a [**un'interfaccia ID3D11ClassLinkage.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





