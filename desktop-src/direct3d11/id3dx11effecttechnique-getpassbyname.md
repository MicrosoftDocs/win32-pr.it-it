---
title: Metodo ID3DX11EffectTechnique GetPassByName (D3dx11effect. h)
description: Ottenere un passaggio per nome.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Metodo GetPassByName Direct3D 11
- Metodo GetPassByName Direct3D 11, interfaccia ID3DX11EffectTechnique
- Interfaccia ID3DX11EffectTechnique Direct3D 11, metodo GetPassByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bbe9b954efff12e458ee6172665118a7b8ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995972"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a>Metodo ID3DX11EffectTechnique:: GetPassByName

Ottenere un passaggio per nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome del passaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Puntatore a un [**ID3DX11EffectPass**](id3dx11effectpass.md).

## <a name="remarks"></a>Commenti

Una tecnica contiene uno o più passaggi. ottenere un pass usando un nome o un indice.

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

