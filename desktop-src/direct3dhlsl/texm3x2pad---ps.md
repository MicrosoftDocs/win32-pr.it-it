---
title: texm3x2pad - ps
description: Esegue la moltiplicazione della prima riga di una matrice di due righe. Questa istruzione deve essere combinata con texm3x2tex - ps o texm3x2depth - ps. Per informazioni dettagliate sull'uso di texmpad, vedere una di queste istruzioni.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55943d2a62f49e6bdb45d893385f0824898d665ee4a4065c4f8c8ed75c2f8249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485441"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad - ps

Esegue la moltiplicazione della prima riga di una matrice di due righe. Questa istruzione deve essere combinata con [texm3x2tex - ps](texm3x2tex---ps.md) o [texm3x2depth - ps](texm3x2depth---ps.md). Per informazioni dettagliate sull'uso di texmpad, vedere una di queste istruzioni.

## <a name="syntax"></a>Sintassi



| tex3x2pad dst, src |
|--------------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione non può essere usata da sola.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




