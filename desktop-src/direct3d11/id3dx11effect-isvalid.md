---
title: Metodo ID3DX11Effect IsValid (D3dx11effect.h)
description: Testare un effetto per verificare se contiene una sintassi valida. | Metodo Id3DX11Effect IsValid (D3dx11effect.h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- Metodo IsValid Direct3D 11
- Metodo IsValid Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo IsValid
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d49cff0f745caddf571b0f0e8d3d2d351d8a90058335611c43edd89f79d84810
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608791"
---
# <a name="id3dx11effectisvalid-method"></a>Metodo ID3DX11Effect::IsValid

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

