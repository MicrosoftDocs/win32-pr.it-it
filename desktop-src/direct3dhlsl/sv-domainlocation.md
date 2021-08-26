---
title: SV_DomainLocation
description: Definisce la posizione sullo scafo del punto di dominio corrente da valutare.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 481d4def3d13ee69138f31adaae3c7d90c2e27ab11702fe3191db94540d9835c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067531"
---
# <a name="sv_domainlocation"></a>SV \_ DomainLocation

Definisce la posizione sullo scafo del punto di dominio corrente da valutare.

## <a name="type"></a>Tipo



| Tipo       | Topologia di input               |
|--------|----------------|
| float2 | quad patch     |
| float3 | tri patch      |
| float2 | isoline        |



 

## <a name="remarks"></a>Commenti

Questo valore di sistema è obbligatorio.

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      | x      |          |       |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Semantica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




