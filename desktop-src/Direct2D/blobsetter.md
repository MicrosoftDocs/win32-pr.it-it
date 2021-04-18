---
title: BlobSetter (D2d1effecthelpers. h)
description: Chiama un callback del setter della proprietà della funzione membro per una proprietà di tipo BLOB.
ms.assetid: 29411D53-1D27-4040-A3C0-B1511E627A32
keywords:
- Direct2D BlobSetter
topic_type:
- apiref
api_name:
- BlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a073db2fb53fa86414ed6081ede0e24c2eb7dcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325091"
---
# <a name="blobsetter"></a>BlobSetter

Chiama un callback del setter della proprietà della funzione membro per una proprietà di tipo BLOB.

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobSetter(
    _In_ IUnknown *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Direct2D:: BlobGetter**](blobgetter.md)
</dt> </dl>

 

 





