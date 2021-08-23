---
title: Metodo DESTROY ID3DX11DataProcessor (D3DX11core.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Elimina il processore dopo il completamento di un elemento di lavoro.
ms.assetid: 759641c0-ef86-42ee-88b9-3fcb7a171d86
keywords:
- Metodo Destroy Direct3D 11
- Metodo Destroy Direct3D 11, interfaccia ID3DX11DataProcessor
- ID3DX11DataProcessor interface Direct3D 11 , Destroy method
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0968ff090f01a27cb18d3fff0e6dbd499c05c95cd558a2eba805dd91a153c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632927"
---
# <a name="id3dx11dataprocessordestroy-method"></a>Metodo ID3DX11DataProcessor::D estroy

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Elimina il processore dopo il completamento di un elemento di lavoro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Destroy();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questo metodo viene usato da [**un'interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





