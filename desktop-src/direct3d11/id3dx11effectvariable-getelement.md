---
title: Metodo GetElement ID3DX11EffectVariable (D3dx11effect. h)
description: Ottiene un elemento di matrice.
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- Metodo GetElement Direct3D 11
- Metodo GetElement Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, Metodo GetElement
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b887bb9e4c1d40f4d3eb0d36b9a7b4d2698b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982136"
---
# <a name="id3dx11effectvariablegetelement-method"></a>Metodo ID3DX11EffectVariable:: GetElement

Ottiene un elemento di matrice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero; in caso contrario, 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Commenti

Se la variabile Effect è una matrice, usare questo metodo per restituire uno degli elementi.

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

