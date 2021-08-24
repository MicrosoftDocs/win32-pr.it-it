---
title: Metodo ID3DX11EffectTechnique GetPassByIndex (D3dx11effect.h)
description: Ottenere un passaggio per indice.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Metodo GetPassByIndex Direct3D 11
- Metodo GetPassByIndex Direct3D 11, interfaccia ID3DX11EffectTechnique
- ID3DX11EffectTechnique interface Direct3D 11 , GetPassByIndex method
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd22cd5e7745b8e5a11018b930f6b544036780b118e9c745b67e730b693cdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565791"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a>Metodo ID3DX11EffectTechnique::GetPassByIndex

Ottenere un passaggio per indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Puntatore a [**id3DX11EffectPass.**](id3dx11effectpass.md)

## <a name="remarks"></a>Commenti

Una tecnica contiene uno o più passaggi. Ottenere un passaggio usando un nome o un indice.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

