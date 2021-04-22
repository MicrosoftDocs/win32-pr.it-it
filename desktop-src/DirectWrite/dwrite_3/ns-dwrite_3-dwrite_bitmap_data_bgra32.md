---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Rappresenta i dati bitmap in formato BGRA32.
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: 3d5b2168e5154f2e55b6f5acb83897f68d4a029c
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881830"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a>DWRITE_BITMAP_DATA_BGRA32 struttura (dwrite_3.h)

Rappresenta i dati bitmap in formato BGRA32.

> [!IMPORTANT]
> Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md) DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme. Per altre informazioni ed esempi di codice, vedi [Panoramica di DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)

## <a name="syntax"></a>Sintassi

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a>Members

`width`

Tipo: **[UINT32](../../winprog/windows-data-types.md)**

Larghezza, in pixel, della bitmap.


`height`

Tipo: **[UINT32](../../winprog/windows-data-types.md)**

Altezza, in pixel, della bitmap.


`pixels`

Tipo: \_ Dimensioni \_ campo \_ (larghezza * altezza)**[UINT32](../../winprog/windows-data-types.md)\***

Puntatore alla posizione dei valori di bit per la bitmap.


## <a name="examples"></a>Esempio

Vedere [l'argomento di panoramica DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Windows 10, Project Dispositivi [app Win32] |
| **Intestazione** | dwrite_3.h (includere dwrite_core.h) |