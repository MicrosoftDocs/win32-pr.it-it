---
description: Crea un oggetto del tipo di carattere. Nota invece di usare questa funzione, è consigliabile usare DirectWrite e la libreria DirectXTK, SpriteFont Class.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Funzione D3DX10CreateFontIndirect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354484"
---
# <a name="d3dx10createfontindirect-function"></a>D3DX10CreateFontIndirect (funzione)

Crea un oggetto del tipo di carattere.

> [!Note]  
> Invece di usare questa funzione, è consigliabile usare [DirectWrite](../directwrite/direct-write-portal.md) e la libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteFont** .

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore a un'interfaccia di [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

</dd> <dt>

*pDesc* \[ in\]
</dt> <dd>

Tipo: **const [**d3dx10 \_ Font \_ desc**](d3dx10-font-desc.md) \***

Puntatore a una struttura [**d3dx10 del \_ tipo di carattere \_ Descrizione**](d3dx10-font-desc.md) , che descrive gli attributi dell'oggetto tipo di carattere da creare. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateFontIndirectW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateFontIndirectA perché vengono utilizzate le stringhe ANSI.

</dd> <dt>

*ppFont* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Restituisce un puntatore a un' [**interfaccia ID3DX10Font**](id3dx10font.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
