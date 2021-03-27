---
title: texm3x2pad-PS
description: Esegue la moltiplicazione della prima riga di una matrice a due righe. Questa istruzione deve essere combinata con texm3x2tex-PS o texm3x2depth-PS. Per informazioni dettagliate sull'uso di texmpad, fare riferimento a una di queste istruzioni.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857786"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad-PS

Esegue la moltiplicazione della prima riga di una matrice a due righe. Questa istruzione deve essere combinata con [texm3x2tex-PS](texm3x2tex---ps.md) o [texm3x2depth-PS](texm3x2depth---ps.md). Per informazioni dettagliate sull'uso di texmpad, fare riferimento a una di queste istruzioni.

## <a name="syntax"></a>Sintassi



| tex3x2pad DST, src |
|--------------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione non può essere usata da sola.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




