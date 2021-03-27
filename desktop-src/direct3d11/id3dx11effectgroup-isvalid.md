---
title: Metodo ID3DX11EffectGroup IsValid (D3dx11effect. h)
description: Testare un effetto per verificare se contiene una sintassi valida. | Metodo ID3DX11EffectGroup IsValid (D3dx11effect. h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- Metodo IsValid-Direct3D 11
- Metodo IsValid, Direct3D 11, interfaccia ID3DX11EffectGroup
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
ms.openlocfilehash: b0d1fd110a0f35f8a288517d72b69a6f5ad9f0ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982283"
---
# <a name="id3dx11effectgroupisvalid-method"></a>Metodo ID3DX11EffectGroup:: IsValid

Testare un effetto per verificare se contiene una sintassi valida.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** se la sintassi del codice è valida. in caso contrario, **false**.

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

