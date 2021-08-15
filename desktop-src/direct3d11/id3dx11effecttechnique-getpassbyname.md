---
title: Metodo ID3DX11EffectTechnique GetPassByName (D3dx11effect.h)
description: Ottenere un pass by name.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Metodo GetPassByName Direct3D 11
- Metodo GetPassByName Direct3D 11, interfaccia ID3DX11EffectTechnique
- ID3DX11EffectTechnique interface Direct3D 11 , GetPassByName method
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
ms.openlocfilehash: dfad489fe6c4eda8ea417a9f272bcc0a7d4035eb04bc675cf599e4f5381234db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532363"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a>Metodo ID3DX11EffectTechnique::GetPassByName

Ottenere un pass by name.

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

 

