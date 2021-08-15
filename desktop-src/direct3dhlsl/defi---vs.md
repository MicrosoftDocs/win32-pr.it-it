---
title: defi - vs
description: Definisce un valore costante integer che deve essere caricato ogni volta che uno shader viene impostato su un dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5568a9d1db49dadb9e0e6497cfd4e5af357054f930c35ec6a7e05d59d5f60965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726681"
---
# <a name="defi---vs"></a>defi - vs

Definisce un valore costante integer che deve essere caricato ogni volta che uno shader viene impostato su un dispositivo.

## <a name="syntax"></a>Sintassi



| defi dst, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   dst è il registro di destinazione.
-   integerValue \# è un valore intero costante.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Defi                   |      | x    | x    | x     | x    | x     |



 

L'istruzione defi definisce una costante integer shader il cui valore viene caricato ogni volta che uno shader viene impostato su un dispositivo. Queste sono chiamate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetVertexShaderConstantI.

Esistono due modi per impostare una costante integer in uno shader.

1.  Usare defi per definire il vettore costante integer direttamente all'interno di uno shader.
2.  Usare i metodi API per impostare una costante.
    -   Usare [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) per impostare una costante integer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def - vs](def---vs.md)
</dt> <dt>

[defb - vs](defb---vs.md)
</dt> </dl>

 

 