---
title: Metodo Apply ID3DX11EffectPass (D3dx11effect. h)
description: Impostare lo stato contenuto in un passaggio al dispositivo.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Applicare il metodo Direct3D 11
- Apply Method Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo Apply
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a061609953e164524e16722222a5ecea81f275b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982250"
---
# <a name="id3dx11effectpassapply-method"></a>Metodo ID3DX11EffectPass:: Apply

Impostare lo stato contenuto in un passaggio al dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Non utilizzato.

</dd> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**Sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a cui applicare il passaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

