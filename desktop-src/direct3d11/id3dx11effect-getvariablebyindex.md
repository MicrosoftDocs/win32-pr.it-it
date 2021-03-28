---
title: Metodo ID3DX11Effect GetVariableByIndex (D3dx11effect. h)
description: Ottiene una variabile in base all'indice.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Metodo GetVariableByIndex Direct3D 11
- Metodo GetVariableByIndex Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetVariableByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996101"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a>Metodo ID3DX11Effect:: GetVariableByIndex

Ottiene una variabile in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Commenti

Un effetto può contenere una o più variabili. Le variabili al di fuori di una tecnica sono considerate globali per tutti gli effetti, quelle situate all'interno di una tecnica sono locali a tale tecnica. È possibile accedere a qualsiasi variabile locale di effetto non statico usando il nome o un indice.

Il metodo restituisce un puntatore a un' [**interfaccia di variabile di effetto**](id3dx11effectvariable.md) se non viene trovata una variabile. è possibile chiamare [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) per verificare se l'indice esiste o meno.

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

 

