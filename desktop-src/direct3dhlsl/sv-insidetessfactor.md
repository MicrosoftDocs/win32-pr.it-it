---
title: SV_InsideTessFactor
description: Definisce l'importo a mosaico all'interno di una superficie della patch.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976210"
---
# <a name="sv_insidetessfactor"></a>\_INSIDETESSFACTOR SV

Definisce l'importo a mosaico all'interno di una superficie della patch.

## <a name="type"></a>Tipo



|            |                |
|------------|----------------|
| Tipo       | Topologia di input |
| float \[ 2\] | patch quad     |
| float      | patch Tri      |
| unused     | isolinea        |



 

I fattori a mosaico devono essere dichiarati come matrici; non possono essere compressi in un singolo vettore.

## <a name="remarks"></a>Commenti

Questo valore deve essere definito durante la funzione costante patch dello scafo shader.

Valore di output necessario per Hull shader se si usano patch quad o tri. Questo valore è un input obbligatorio per lo shader del dominio in modo che l'hardware corrisponda alle firme tramite il mosaico.

Questa funzione è supportata nei tipi di shader seguenti:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Semantica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




