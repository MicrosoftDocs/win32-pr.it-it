---
description: Genera una catena mipmap usando un filtro di trama specifico.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Funzione D3DX10FilterTexture (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 225caf2c9b08a498e77723dbb7ab43c8fd4850262c1f58f5ae37a3157e953edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497641"
---
# <a name="d3dx10filtertexture-function"></a>Funzione D3DX10FilterTexture

Genera una catena mipmap usando un filtro di trama specifico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Oggetto trama da filtrare. Vedere [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*SrcLevel* 
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Livello mipmap i cui dati vengono usati per generare il resto della catena mipmap.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Flag che controllano la modalità di filtro di ogni miplevel (o D3DX10 \_ DEFAULT per D3DX10 \_ FILTER \_ BOX). Vedere [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
