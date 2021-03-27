---
title: defb-PS
description: Definisce un valore costante booleano che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729175"
---
# <a name="defb---ps"></a>defb-PS

Definisce un valore costante booleano che deve essere caricato ogni volta che uno shader è impostato su un dispositivo.

## <a name="syntax"></a>Sintassi



| defb dest, booleanValue |
|-------------------------|



 

dove

-   DST è il registro di destinazione.
-   booleanValue è un singolo valore booleano, ovvero true o false.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defb                  |      |      |      |      |      | x    | x     | x    | x     |



 

L'istruzione defb definisce una costante dello shader booleano il cui valore viene caricato ogni volta che uno shader è impostato su un dispositivo. Sono denominate costanti immediate. Le costanti immediate hanno la precedenza sulle costanti impostate dal metodo API SetPixelShaderConstantB.

Esistono due modi per impostare un booleanconstant in uno shader.

1.  Usare defb per definire la costante direttamente all'interno di uno shader.
2.  Usare i metodi API per impostare una costante.
    -   Usare [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) per impostare una costante booleana.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[def-PS](def---ps.md)
</dt> <dt>

[defi-PS](defi---ps.md)
</dt> </dl>

 

 