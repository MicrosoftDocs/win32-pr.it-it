---
title: Metodo ID3DX11EffectSamplerVariable GetBackingStore (D3dx11effect.h)
description: Ottenere un puntatore a una variabile che contiene lo stato del campionatore.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Metodo GetBackingStore Direct3D 11
- Metodo GetBackingStore Interfaccia Direct3D 11, ID3DX11EffectSamplerVariable
- ID3DX11EffectSamplerVariable interface Direct3D 11 , Metodo GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51bba7ff1c23a7b842fc6f41ea623b19096b4cbf1691e5645d32cc1df02a2bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534167"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a>Metodo ID3DX11EffectSamplerVariable::GetBackingStore

Ottenere un puntatore a una variabile che contiene lo stato del campionatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice in una matrice di descrizioni del campionatore. Se nell'effetto è presente una sola variabile di campionamento, usare 0.

</dd> <dt>

*pSamplerDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***

Puntatore a una descrizione del campionatore (vedere [**D3D11 \_ SAMPLER \_ DESC).**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

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

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

