---
title: ASFLeakyBucketPairs
description: L'attributo ASFLeakyBucketPairs è un attributo facoltativo che descrive i requisiti del buffer per un file di velocità in bit variabile.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- ASFLeakyBucketPairs Windows Media Format
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299151"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

L'attributo **ASFLeakyBucketPairs** è un attributo facoltativo che descrive i requisiti del buffer per un file di velocità in bit variabile.

## <a name="global-constant"></a>Costante globale

g \_ wszASFLeakyBucketPairs

## <a name="data-type"></a>Tipo di dati

**\_binario di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo ha il formato seguente:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Dove *wReserved* deve essere uguale a zero e *bucket* è una matrice di strutture di coppie di bucket a perdita di [**WM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) . La matrice deve contenere almeno due voci, ma può avere dimensioni maggiori. L'oggetto Reader utilizza questo attributo per determinare la quantità di contenuto da memorizzare nel buffer prima della riproduzione.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




