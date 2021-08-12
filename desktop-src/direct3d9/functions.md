---
description: Una funzione è il blocco predefinito per uno shader creato nel linguaggio di alto livello. Se si preferisce scrivere shader in un linguaggio di tipo C anziché nel linguaggio assembly, è necessario scrivere funzioni.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintassi della funzione Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9de680f2f892e59f49e1dfd0850a128ca9ba34e2588e416059251d5058c44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297109"
---
# <a name="effect-function-syntax-direct3d-9"></a>Sintassi della funzione Effect (Direct3D 9)

Una funzione è il blocco predefinito per uno shader creato nel linguaggio di alto livello. Se si preferisce scrivere shader in un linguaggio di tipo C anziché nel linguaggio assembly, è necessario scrivere funzioni.

## <a name="syntax"></a>Sintassi


```
type id ( [ parameters ] )  
    { body }
```



Le funzioni non modificano i valori dei parametri in alcun modo.

-   type: qualsiasi riferimento [valido per il tipo HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)
-   id: nome univoco.
-   parameters: parametri della funzione.
-   body: corpo della funzione.

Le funzioni vengono compilate dal linguaggio di alto livello. Vedere [Informazioni di riferimento per HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
