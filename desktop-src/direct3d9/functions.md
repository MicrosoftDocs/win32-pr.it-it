---
description: Una funzione è il blocco predefinito per uno shader creato nel linguaggio di alto livello. Se si preferisce scrivere shader in un linguaggio di tipo C anziché in un linguaggio assembly, è opportuno scrivere funzioni.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintassi della funzione Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520906"
---
# <a name="effect-function-syntax-direct3d-9"></a>Sintassi della funzione Effect (Direct3D 9)

Una funzione è il blocco predefinito per uno shader creato nel linguaggio di alto livello. Se si preferisce scrivere shader in un linguaggio di tipo C anziché in un linguaggio assembly, è opportuno scrivere funzioni.

## <a name="syntax"></a>Sintassi


```
type id ( [ parameters ] )  
    { body }
```



Le funzioni non modificano i valori dei parametri in un effetto.

-   Type: qualsiasi [riferimento valido per](../direct3dhlsl/dx-graphics-hlsl-reference.md) il tipo HLSL.
-   ID: nome univoco.
-   Parameters-parametri della funzione.
-   Body: corpo della funzione.

Le funzioni sono compilate dal linguaggio di alto livello. Vedere informazioni [di riferimento per HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
