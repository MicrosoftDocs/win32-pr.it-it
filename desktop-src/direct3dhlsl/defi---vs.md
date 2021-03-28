---
title: defi-vs
description: Definisce un valore costante Integer, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517007"
---
# <a name="defi---vs"></a>defi-vs

Definisce un valore costante Integer, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.

## <a name="syntax"></a>Sintassi



| defi DST, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   DST è il registro di destinazione.
-   integerValue \# è un valore intero costante.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| defi                   |      | x    | x    | x     | x    | x     |



 

L'istruzione defi definisce una costante di Integer shader il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo. Sono denominate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetVertexShaderConstantI.

Esistono due modi per impostare una costante Integer in uno shader.

1.  Usare defi per definire il vettore di costanti Integer direttamente all'interno di uno shader.
2.  Usare i metodi API per impostare una costante.
    -   Usare [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) per impostare una costante Integer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def-vs](def---vs.md)
</dt> <dt>

[defb-vs](defb---vs.md)
</dt> </dl>

 

 