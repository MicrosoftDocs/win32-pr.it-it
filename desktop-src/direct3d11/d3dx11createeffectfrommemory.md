---
title: Funzione D3DX11CreateEffectFromMemory (D3dx11effect.h)
description: Crea un effetto da un effetto binario o da un file.
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
ms.openlocfilehash: c99cdef28acae9419a5b597d5be1703ea9e866d521d7f94bb330b151abc74842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124806"
---
# <a name="d3dx11createeffectfrommemory-function"></a>Funzione D3DX11CreateEffectFromMemory

Crea un effetto da un effetto binario o da un file.

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

Tipo: **\* void**

BLOB di dati degli effetti compilati.

</dd> <dt>

*Datalength* 
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Lunghezza del BLOB di dati.

</dd> <dt>

*FXFlags* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Non esistono flag di effetto. Imposta su zero.

</dd> <dt>

*pDevice* 
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntatore [**all'oggetto ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) in cui creare le risorse effect.

</dd> <dt>

*ppEffect* 
</dt> <dd>

Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Indirizzo dell'interfaccia [**ID3DX11Effect**](id3dx11effect.md) appena creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> È necessario usare [l'origine Effects 11](https://github.com/Microsoft/FX11) per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedi Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni effetti 11](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

