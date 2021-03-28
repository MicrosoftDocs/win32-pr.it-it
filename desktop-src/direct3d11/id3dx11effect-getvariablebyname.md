---
title: Metodo ID3DX11Effect GetVariableByName (D3dx11effect. h)
description: Ottenere una variabile in base al nome.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Metodo GetVariableByName Direct3D 11
- Metodo GetVariableByName Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetVariableByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996095"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>Metodo ID3DX11Effect:: GetVariableByName

Ottenere una variabile in base al nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome della variabile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Restituisce una variabile non valida se non è possibile trovare il nome specificato.

## <a name="remarks"></a>Commenti

Un effetto può contenere una o più variabili. Le variabili al di fuori di una tecnica sono considerate globali per tutti gli effetti, quelle situate all'interno di una tecnica sono locali a tale tecnica. È possibile accedere a una variabile Effect usando il nome o un indice.

Il metodo restituisce un puntatore a un' [**interfaccia della variabile di effetto**](id3dx11effectvariable.md) indipendentemente dal fatto che venga trovata o meno una variabile. È necessario chiamare [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) per verificare se il nome esiste o meno.

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

 

