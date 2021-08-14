---
title: ASFLeakyBucketPairs
description: L'attributo ASFLeakyBucketPairs è un attributo facoltativo che descrive i requisiti di memorizzazione nel buffer per un file a velocità in bit variabile.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- ASFLeakyBucketPairs windows Media Format
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76de649a069b0cfec74fabe1a41d6cfa659b39448257a4bc966065e1bce98ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434620"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

**L'attributo ASFLeakyBucketPairs** è un attributo facoltativo che descrive i requisiti di memorizzazione nel buffer per un file a velocità in bit variabile.

## <a name="global-constant"></a>Costante globale

g \_ wszASFLeakyBucketPairs

## <a name="data-type"></a>Tipo di dati

**FILE \_ BINARIO DI TIPO WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo ha il formato seguente:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Dove *wReserved deve* essere uguale a zero e *bucket* è una matrice di strutture [**BUCKET PAIR WM \_ \_ \_ LEAKY.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) La matrice deve contenere almeno due voci, ma può essere più grande. L'oggetto lettore usa questo attributo per determinare la quantità di contenuto da bufferare prima della riproduzione.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




