---
title: Metodo ID3DX11Effect GetGroupByIndex (D3dx11effect.h)
description: Ottiene un gruppo di effetti in base all'indice.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Metodo GetGroupByIndex Direct3D 11
- Metodo GetGroupByIndex Direct3D 11, interfaccia ID3DX11Effect
- ID3DX11Effect interface Direct3D 11 , GetGroupByIndex method
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184971eea69f80f105aa29bb3dac9decbeb18d3452ca29656a150d4f1e5d9e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632471"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a>Metodo ID3DX11Effect::GetGroupByIndex

Ottiene un gruppo di effetti in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice del gruppo di effetti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Puntatore a [**un'interfaccia ID3DX11EffectGroup.**](id3dx11effectgroup.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

