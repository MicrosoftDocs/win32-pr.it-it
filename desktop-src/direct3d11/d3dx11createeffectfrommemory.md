---
title: Funzione D3DX11CreateEffectFromMemory (D3dx11effect. h)
description: Crea un effetto da un file o un effetto binario.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- Funzione D3DX11CreateEffectFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996011"
---
# <a name="d3dx11createeffectfrommemory-function"></a>D3DX11CreateEffectFromMemory (funzione)

Crea un effetto da un file o un effetto binario.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **void \***

BLOB di dati degli effetti compilati.

</dd> <dt>

*DataLength* 
</dt> <dd>

Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**

Lunghezza del BLOB di dati.

</dd> <dt>

*FXFlags* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nessun flag di effetto esistente. Imposta su zero.

</dd> <dt>

*pDevice* 
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntatore a [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) su cui creare le risorse di effetto.

</dd> <dt>

*ppEffect* 
</dt> <dd>

Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Indirizzo dell'interfaccia [**ID3DX11Effect**](id3dx11effect.md) appena creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> È necessario usare [Effects 11 source](https://github.com/Microsoft/FX11) per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni Effects 11](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

