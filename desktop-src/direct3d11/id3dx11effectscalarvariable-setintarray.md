---
title: Metodo ID3DX11EffectScalarVariable SetIntArray (D3dx11effect. h)
description: Impostare una matrice di variabili Integer.
ms.assetid: 27efb643-0762-4cd7-84ad-f82b2bb1584a
keywords:
- Metodo SetIntArray Direct3D 11
- Metodo SetIntArray Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- Interfaccia ID3DX11EffectScalarVariable Direct3D 11, metodo SetIntArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetIntArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142a1686b9dde8f6a2c8f41d521ac085bd403ec0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982154"
---
# <a name="id3dx11effectscalarvariablesetintarray-method"></a>Metodo ID3DX11EffectScalarVariable:: SetIntArray

Impostare una matrice di variabili Integer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIntArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Puntatore all'inizio dei dati da impostare.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Deve essere impostato su 0; Questa operazione è riservata per un utilizzo futuro.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi di matrice da impostare.

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

