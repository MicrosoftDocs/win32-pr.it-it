---
title: Metodo ID3DX11Effect GetVariableByName (D3dx11effect.h)
description: Ottenere una variabile in base al nome.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Metodo GetVariableByName Direct3D 11
- Metodo GetVariableByName Direct3D 11, interfaccia ID3DX11Effect
- ID3DX11Effect interfaccia Direct3D 11, metodo GetVariableByName
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
ms.openlocfilehash: b3e8741eaf2ced1022a130ecb94c7f8553159e862ca23b50ba4d12786ad37620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099044"
---
# <a name="id3dx11effectgetvariablebyname-method"></a>Metodo ID3DX11Effect::GetVariableByName

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

Puntatore a [**id3DX11EffectVariable.**](id3dx11effectvariable.md) Restituisce una variabile non valida se non è possibile trovare il nome specificato.

## <a name="remarks"></a>Commenti

Un effetto può contenere una o più variabili. Le variabili all'esterno di una tecnica sono considerate globali per tutti gli effetti, quelle che si trovano all'interno di una tecnica sono locali rispetto a tale tecnica. È possibile accedere a una variabile dell'effetto usandone il nome o con un indice.

Il metodo restituisce un puntatore a [**un'interfaccia effect-variable**](id3dx11effectvariable.md) indipendentemente dal fatto che sia stata trovata o meno una variabile. [**Id3DX11Effect::IsValid**](id3dx11effect-isvalid.md) deve essere chiamato per verificare se il nome esiste o meno.

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

 

