---
title: Metodo GetDevice ID3DX11Effect (D3dx11effect. h)
description: Ottenere il dispositivo che ha creato l'effetto.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Metodo GetDevice Direct3D 11
- Metodo GetDevice Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetDevice
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235150"
---
# <a name="id3dx11effectgetdevice-method"></a>Metodo ID3DX11Effect:: GetDevice

Ottenere il dispositivo che ha creato l'effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDevice* 
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***

Puntatore a un [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Viene creato un effetto per un dispositivo specifico, chiamando una funzione come [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

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

 

 





