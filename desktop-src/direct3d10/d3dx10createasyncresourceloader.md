---
description: Creare un caricatore di risorse asincrono.
ms.assetid: 1b3eb21c-4ba6-4910-b2f0-2ffa4ae50e47
title: Funzione D3DX10CreateAsyncResourceLoader (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncResourceLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bedb3559ead576c074dafed526fc0ebfefebaf5c3e53a6559223af346e7f9c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303456"
---
# <a name="d3dx10createasyncresourceloader-function"></a>Funzione D3DX10CreateAsyncResourceLoader

Creare un caricatore di risorse asincrono.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle per il modulo della risorsa. Usare [la funzione GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per ottenere l'handle.

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome della risorsa in hSrcModule. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> <dt>

*ppDataLoader* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Indirizzo di un puntatore al processore di dati asincrono (vedere [**l'interfaccia ID3DX10DataProcessor).**](id3dx10dataprocessor.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
