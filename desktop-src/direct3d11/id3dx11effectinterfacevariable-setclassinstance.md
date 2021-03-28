---
title: Metodo ID3DX11EffectInterfaceVariable SetClassInstance (D3dx11effect. h)
description: Imposta un'istanza della classe.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Metodo SetClassInstance Direct3D 11
- Metodo SetClassInstance Direct3D 11, interfaccia ID3DX11EffectInterfaceVariable
- Interfaccia ID3DX11EffectInterfaceVariable Direct3D 11, metodo SetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982274"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a>Metodo ID3DX11EffectInterfaceVariable:: SetClassInstance

Imposta un'istanza della classe.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pEffectClassInstance* 
</dt> <dd>

Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***

Puntatore a un'interfaccia [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) .

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

[ID3DX11EffectInterfaceVariable](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





