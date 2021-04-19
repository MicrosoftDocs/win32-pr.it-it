---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: 'IDWriteBitmapRenderTarget2:: getbitmapdata (dwrite_3. h)'
description: Recupera i dati pixel da una destinazione di rendering bitmap.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: dff9904eef692b3858cc044f7b400a5b3641456a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320349"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a>Metodo IDWriteBitmapRenderTarget2:: getbitmapdata (dwrite_3. h)

Recupera i dati pixel da una destinazione di rendering bitmap.

> [!IMPORTANT]
> Questa API è disponibile come parte dell'implementazione di DWriteCore di [DirectWrite](../direct-write-portal.md). DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme. Per altre informazioni ed esempi di codice, vedere [Panoramica di DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Sintassi

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a>Parametri

`bitmapData`

Tipo: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***

Puntatore ai dati pixel.

## <a name="return-value"></a>Valore restituito

Tipo: <b>HRESULT</b>

Se questo metodo ha esito positivo, restituisce <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. In caso contrario, restituisce un codice di errore <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .

## <a name="examples"></a>Esempio

Vedere l'argomento [Panoramica di DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Windows 10, Project Reunion 0,1 versione provvisoria [app Win32] |
| **Intestazione** | dwrite_3. h (includere dwrite_core. h) |
| **Libreria** | DWrite. lib |
| **DLL** | Dwrite.dll |

## <a name="see-also"></a>Vedi anche

[IDWriteBitmapRenderTarget2](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)