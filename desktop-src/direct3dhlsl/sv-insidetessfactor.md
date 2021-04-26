---
title: SV_InsideTessFactor
description: Definisce la quantità a tessellazione all'interno di una superficie patch.
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
ms.openlocfilehash: 4d047f7961868de020ac50ffce22b6ce02d078a5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996918"
---
# <a name="sv_insidetessfactor"></a>SV \_ InsideTessFactor

Definisce la quantità a tessellazione all'interno di una superficie patch.

## <a name="type"></a>Tipo



|            |                |
|------------|----------------|
| Tipo       | Topologia di input |
| float \[ 2\] | quad patch     |
| float      | tri patch      |
| unused     | isoline        |



 

I fattori a tessellazione devono essere dichiarati come matrice. non possono essere suddivisi in un singolo vettore.

## <a name="remarks"></a>Commenti

Questo valore deve essere definito durante la funzione costante patch dello hull shader.

Valore di output obbligatorio per lo hull shader se si usano patch quad o tri. Questo valore è un input obbligatorio per lo shader del dominio in modo che l'hardware corrisponda alle firme tramite il tessellatore.

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Semantica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




