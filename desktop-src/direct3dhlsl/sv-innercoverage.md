---
title: SV_InnerCoverage
description: SV \_ InputCoverage rappresenta le informazioni di rasterizzazione conservative sottostimate, ad esempio se un pixel è garantito per essere completamente coperto.
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
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993549"
---
# <a name="sv_innercoverage"></a>\_INNERCOVERAGE SV

SV \_ InputCoverage rappresenta le informazioni di rasterizzazione conservative sottostimate, ad esempio se un pixel è garantito per essere completamente coperto.

## <a name="type"></a>Tipo



|      |
|------|
| Tipo |
| uint |



 

## <a name="remarks"></a>Commenti

Questo valore generato dal sistema è richiesto per il supporto di livello 3 ed è disponibile solo in tale livello. Questo input si escludono a vicenda con SV \_ coverage. non è possibile usare entrambi.

Per accedere a SV \_ InnerCoverage, è necessario dichiararlo come componente singolo da uno dei registri di input pixel shader. La modalità di interpolazione nella dichiarazione deve essere costante (l'interpolazione non è applicabile).

La rasterizzazione conservativa è disponibile sia in D3D 11.3 che in D3D12. Fare riferimento a:

-   [Rasterizzazione conservativa D3D 11.3](/windows/desktop/direct3d11/conservative-rasterization)
-   [Rasterizzazione conservativa D3D12](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Valori di sistema del modello shader 5,1](shader-model-5-1-system-values.md)
</dt> </dl>

 

 