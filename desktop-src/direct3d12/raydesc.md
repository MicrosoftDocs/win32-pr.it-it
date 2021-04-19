---
description: Passato alla funzione TraceRay per definire l'origine, la direzione e gli extent del raggio.
ms.assetid: ''
title: Struttura RayDesc
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305067"
---
# <a name="raydesc-structure"></a>Struttura RayDesc

Passato alla funzione [**TraceRay**](traceray-function.md) per definire l'origine, la direzione e gli extent del raggio.

## <a name="syntax"></a>Sintassi


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a>Campi

<dl> <dt>

<span id="Origin"></span><span id="origin"></span>**Origine**
</dt> <dd>

Origine del raggio.

</dd> <dt>

<span id="TMin"></span><span id="tmin"></span>**TMin**
</dt> <dd>

Extent minimo del raggio.


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**Direzione**
</dt> <dd>

Direzione del raggio.


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**TMax**
</dt> <dd>

Extent massimo del raggio.


</dd>

## <a name="requirements"></a>Requisiti



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




