---
title: defb-vs
description: Definisce un valore costante booleano che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963108"
---
# <a name="defb---vs"></a>defb-vs

Definisce un valore costante booleano che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.

## <a name="syntax"></a>Sintassi



| defb dest, booleanValue |
|-------------------------|



 

dove

-   DST è il registro di destinazione.
-   booleanValue è un valore booleano, ovvero true o false.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| defb                   |      | x    | x    | x     | x    | x     |



 

L'istruzione defb-vs definisce una costante dello shader booleano il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo. Sono denominate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetVertexShaderConstantB.

Esistono due modi per impostare una costante booleana in uno shader.

1.  Usare defb-vs per definire la costante direttamente all'interno di uno shader.
2.  Usare i metodi API per impostare una costante.
    -   Usare [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) per impostare una costante booleana.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def-vs](def---vs.md)
</dt> <dt>

[defi-vs](defi---vs.md)
</dt> </dl>

 

 