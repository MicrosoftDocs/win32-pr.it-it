---
title: Metodo ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
description: Ottenere una tecnica in base al nome. | Metodo ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Metodo GetTechniqueByName Direct3D 11
- Metodo GetTechniqueByName Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982418"
---
# <a name="id3dx11effectgettechniquebyname-method"></a>Metodo ID3DX11Effect:: GetTechniqueByName

Ottenere una tecnica in base al nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome della tecnica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Puntatore a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md). Se non viene trovata una tecnica con il nome appropriato, viene restituita una tecnica non valida. Per determinare se è valido, è necessario chiamare [**ID3DX11EffectTechnique:: IsValid**](id3dx11effecttechnique-isvalid.md) sulla tecnica restituita.

## <a name="remarks"></a>Commenti

Un effetto contiene una o più tecniche. ogni tecnica contiene uno o più passaggi. È possibile accedere a una tecnica usando il nome o un indice.

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

 

