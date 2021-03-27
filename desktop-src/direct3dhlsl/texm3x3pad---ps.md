---
title: texm3x3pad-PS
description: Esegue la prima o la seconda moltiplicazione di riga di una matrice a tre righe di moltiplicazione. Questa istruzione deve essere usata in combinazione con texm3x3-PS, texm3x3spec-PS, texm3x3vspec-PS o texm3x3tex-PS.
ms.assetid: 375526ee-cd58-4179-9b21-c63f17282f6b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0013c4d2baf9a404406982b5a8e984698a964f33
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398235"
---
# <a name="texm3x3pad---ps"></a>texm3x3pad-PS

Esegue la prima o la seconda moltiplicazione di riga di una matrice a tre righe di moltiplicazione. Questa istruzione deve essere usata in combinazione con [texm3x3-PS](texm3x3---ps.md), [texm3x3spec-PS](texm3x3spec---ps.md), [texm3x3vspec-PS](texm3x3vspec---ps.md)o [texm3x3tex-PS](texm3x3tex---ps.md).

## <a name="syntax"></a>Sintassi



| texm3x3pad DST, src |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3pad            | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione non può essere usata da sola.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




