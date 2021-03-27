---
title: Metodo ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
description: Ottenere un'annotazione in base al nome. | Metodo ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Metodo GetAnnotationByName Direct3D 11
- Metodo GetAnnotationByName Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37efcd773728e563a4112f61a7c6c965d05bad4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355119"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a>Metodo ID3DX11EffectVariable:: GetAnnotationByName

Ottenere un'annotazione in base al nome.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome dell'annotazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Si noti che se l'annotazione non viene trovata, il **ID3DX11EffectVariable** restituito sarà vuoto. È necessario chiamare il metodo [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) per determinare se l'annotazione è stata trovata.

## <a name="remarks"></a>Commenti

Annonations può essere collegato a una tecnica, a un passaggio o a una variabile globale.

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

 

