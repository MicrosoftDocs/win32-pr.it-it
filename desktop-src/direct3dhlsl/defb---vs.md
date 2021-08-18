---
title: defb - vs
description: Definisce un valore costante booleano, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e5ace74e275ae63a62306d47d50924e9c4e9a9771027e75659ef72345f69906d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792673"
---
# <a name="defb---vs"></a>defb - vs

Definisce un valore costante booleano, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.

## <a name="syntax"></a>Sintassi



| defb dest, booleanValue |
|-------------------------|



 

dove

-   dst è il registro di destinazione.
-   booleanValue è un valore booleano, True o False.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| defb                   |      | x    | x    | x     | x    | x     |



 

L'istruzione defb - vs definisce una costante shader booleana il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo. Queste sono chiamate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetVertexShaderConstantB.

Esistono due modi per impostare una costante booleana in uno shader.

1.  Usare defb - vs per definire la costante direttamente all'interno di uno shader.
2.  Usare i metodi API per impostare una costante.
    -   Usare [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) per impostare una costante booleana.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def - vs](def---vs.md)
</dt> <dt>

[defi - vs](defi---vs.md)
</dt> </dl>

 

 