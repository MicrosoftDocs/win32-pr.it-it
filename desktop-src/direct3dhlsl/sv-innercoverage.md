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
ms.openlocfilehash: e1ac278f0524446b5171ef278e169fbe7c3a082f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996968"
---
# <a name="sv_innercoverage"></a>SV \_ InnerCoverage

SV InputCoverage rappresenta informazioni di rasterizzazione conservative sottostimate,ad esempio se un pixel è garantito per essere \_ completamente coperto.

## <a name="type"></a>Tipo



|      |
|------|
| Tipo |
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

 

 
