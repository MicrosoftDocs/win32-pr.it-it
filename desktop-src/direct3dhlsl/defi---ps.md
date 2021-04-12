---
title: defi-PS
description: Definisce un valore costante Integer, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118187"
---
# <a name="defi---ps"></a>defi-PS

Definisce un valore costante Integer, che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.

## <a name="syntax"></a>Sintassi



| defi DST, integerValue |
|------------------------|



 

-   DST è il registro di destinazione.
-   integerValue è un valore intero costante.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defi                  |      |      |      |      |      | x    | x     | x    | x     |



 

L'istruzione defi definisce una costante dello shader il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo. Sono denominate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetPixelShaderConstantB.

Esistono due modi per impostare una costante in uno shader.

1.  Usare defi per definire la costante direttamente all'interno di uno shader.
2.  Usare i metodi API per impostare una costante.
    -   Usare [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) per impostare una costante booleana.
    -   Usare [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) per impostare una costante a virgola mobile.
    -   Usare [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) per impostare una costante Integer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 