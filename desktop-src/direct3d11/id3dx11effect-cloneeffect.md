---
title: Metodo CloneEffect ID3DX11Effect (D3dx11effect.h)
description: Crea una copia di un'interfaccia effetto.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Metodo CloneEffect Direct3D 11
- Metodo CloneEffect Direct3D 11, interfaccia ID3DX11Effect
- INTERFACCIA ID3DX11Effect Direct3D 11, metodo CloneEffect
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fa68fe05674573468eb684d8149d8dae45e540572f4d777bb860755c60e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124526"
---
# <a name="id3dx11effectcloneeffect-method"></a>Metodo ID3DX11Effect::CloneEffect

Crea una copia di un'interfaccia effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flag che influiscono sulla creazione dell'effetto clonato. Può essere 0 o uno dei valori seguenti.



| Flag                                    | Descrizione                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX11 \_ EFFECT \_ CLONE \_ FORCE \_ NONSINGLE | Ignorare tutti i qualificatori "singoli" in cbuffer. Tutti i cbuffer avranno il proprio [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)creato nell'effetto clonato. |



 

</dd> <dt>

*ppClonedEffect* 
</dt> <dd>

Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Puntatore a [**un puntatore ID3DX11Effect**](id3dx11effect.md) che verrà impostato sulla copia dell'effetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

