---
title: SV_InnerCoverage
description: SV InputCoverage rappresenta informazioni di rasterizzazione conservative sottostimate,ad esempio se un pixel è garantito per essere \_ completamente coperto.
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 168f90c17c9e6837d696ebb6dac8f39dc6dfb366
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826625"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

SV InputCoverage rappresenta informazioni di rasterizzazione conservative sottostimate,ad esempio se un pixel è garantito per essere \_ completamente coperto.

## <a name="type"></a>Tipo



| Tipo     |
|------|
| uint |



 

## <a name="remarks"></a>Commenti

Questo valore generato dal sistema è necessario per il supporto di livello 3 ed è disponibile solo in tale livello. Questo input si escludono a vicenda con la copertura SV. Non \_ è possibile usare entrambi.

Per accedere a SV InnerCoverage, deve essere dichiarato come singolo componente di uno dei registri pixel shader \_ input. La modalità di interpolazione nella dichiarazione deve essere costante (l'interpolazione non è applicabile).

La rasterizzazione conservativa è disponibile sia in D3D11.3 che in D3D12. Fare riferimento a:

-   [D3D11.3 Rasterizzazione conservativa](/windows/desktop/direct3d11/conservative-rasterization)
-   [Rasterizzazione conservativa D3D12](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Valori di sistema del modello shader 5.1](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
