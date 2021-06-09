---
title: SV_InsideTessFactor
description: Definisce la quantità di tassellamento all'interno di una superficie patch.
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
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826615"
---
# <a name="sv_insidetessfactor"></a>SV \_ InsideTessFactor

Definisce la quantità di tassellamento all'interno di una superficie patch.

## <a name="type"></a>Tipo



|  Tipo          | Topologia di input               |
|------------|----------------|
| float \[ 2\] | quad patch     |
| float      | tri patch      |
| unused     | isoline        |



 

I fattori di tessellazione devono essere dichiarati come matrice. non possono essere imballate in un singolo vettore.

## <a name="remarks"></a>Commenti

Questo valore deve essere definito durante la funzione costante patch dello hull shader.

Valore di output obbligatorio per lo hull shader se si usano patch quad o tri. Questo valore è un input obbligatorio per lo shader di dominio in modo che l'hardware corrisponda alle firme tramite il tessellatore.

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

 

 




