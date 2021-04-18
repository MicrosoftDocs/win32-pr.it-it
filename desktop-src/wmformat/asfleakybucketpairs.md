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
# <a name="asfleakybucketpairs"></a><span data-ttu-id="a08d9-104">ASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="a08d9-104">ASFLeakyBucketPairs</span></span>

<span data-ttu-id="a08d9-105">L'attributo **ASFLeakyBucketPairs** è un attributo facoltativo che descrive i requisiti del buffer per un file di velocità in bit variabile.</span><span class="sxs-lookup"><span data-stu-id="a08d9-105">The **ASFLeakyBucketPairs** attribute is an optional attribute that describes the buffering requirements for a variable bit rate file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a08d9-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="a08d9-106">Global Constant</span></span>

<span data-ttu-id="a08d9-107">g \_ wszASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="a08d9-107">g\_wszASFLeakyBucketPairs</span></span>

## <a name="data-type"></a><span data-ttu-id="a08d9-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a08d9-108">Data Type</span></span>

<span data-ttu-id="a08d9-109">**\_binario di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="a08d9-109">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="a08d9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a08d9-110">Remarks</span></span>

<span data-ttu-id="a08d9-111">Questo attributo ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="a08d9-111">This attribute has the following format:</span></span>

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="a08d9-112">Dove *wReserved* deve essere uguale a zero e *bucket* è una matrice di strutture di coppie di bucket a perdita di [**WM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) .</span><span class="sxs-lookup"><span data-stu-id="a08d9-112">Where *wReserved* must equal zero, and *bucket* is an array of [**WM\_LEAKY\_BUCKET\_PAIR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) structures.</span></span> <span data-ttu-id="a08d9-113">La matrice deve contenere almeno due voci, ma può avere dimensioni maggiori.</span><span class="sxs-lookup"><span data-stu-id="a08d9-113">The array must contain at least two entries, but can be larger.</span></span> <span data-ttu-id="a08d9-114">L'oggetto Reader utilizza questo attributo per determinare la quantità di contenuto da memorizzare nel buffer prima della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a08d9-114">The reader object uses this attribute to determine the amount of content to buffer before playback.</span></span>

## <a name="see-also"></a><span data-ttu-id="a08d9-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a08d9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08d9-116">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="a08d9-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




