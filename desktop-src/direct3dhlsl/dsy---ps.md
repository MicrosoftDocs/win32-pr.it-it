---
title: DSY-PS
description: Calcola il tasso di modifica nella direzione y della destinazione di rendering.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398218"
---
# <a name="dsy---ps"></a>DSY-PS

Calcola il tasso di modifica nella direzione y della destinazione di rendering.

## <a name="syntax"></a>Sintassi



| DSY DST, src |
|--------------|



 

Dove:

-   DST è un registro di destinazione.
-   src è un registro di origine di input.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DSY                   |      |      |      |      |      | x    | x     | x    | x     |



 

La frequenza delle modifiche calcolate dal registro di origine è un'approssimazione del contenuto dello stesso registro in pixel adiacenti che eseguono il pixel shader in lock-step con il pixel corrente.

Le istruzioni [DSX](dsx---ps.md) e DSY calcolano il risultato esaminando il contenuto corrente del registro di origine (per componente) per i diversi pixel nell'area locale in esecuzione nel passaggio di blocco. La formula esatta utilizzata per calcolare la sfumatura varia in base all'hardware, ma deve essere coerente con il modo in cui l'hardware esegue le stesse operazioni come parte del processo di calcolo del livello di dettaglio per il campionamento della trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-PS](texldd---ps.md)
</dt> </dl>

 

 




