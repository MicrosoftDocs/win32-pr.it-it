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
ms.openlocfilehash: a4fa44e68e8747a0a8366ca2d949290f585d4b70d9e75b4ed2d3b6fdda0d05c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123686"
---
# <a name="raydesc-structure"></a>Struttura RayDesc

Passato alla [**funzione TraceRay**](traceray-function.md) per definire l'origine, la direzione e gli extent del raggio.

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

Estensione minima del raggio.


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**Direzione**
</dt> <dd>

Direzione del raggio.


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**Tmax**
</dt> <dd>

Estensione massima del raggio.


</dd>

## <a name="requirements"></a>Requisiti



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Direct3D 12 Raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




