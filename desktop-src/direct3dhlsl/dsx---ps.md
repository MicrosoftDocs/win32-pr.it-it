---
title: DSX-PS
description: Calcola il tasso di modifica nella direzione x della destinazione di rendering.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 701dbe0125d10850760e6a1f08a2f84a50c55fe2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956081"
---
# <a name="dsx---ps"></a>DSX-PS

Calcola il tasso di modifica nella direzione x della destinazione di rendering.

## <a name="syntax"></a>Sintassi



| DSX DST, src |
|--------------|



 

Dove:

-   DST è un registro di destinazione.
-   src è un registro di origine di input.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DSX                   |      |      |      |      |      | x    | x     | x    | x     |



 

La frequenza delle modifiche calcolate dal registro di origine è un'approssimazione del contenuto dello stesso registro in pixel adiacenti che eseguono il pixel shader in lock-step con il pixel corrente.

Le istruzioni DSX e [DSY](dsy---ps.md) calcolano il risultato esaminando il contenuto corrente del registro di origine (per componente) per i diversi pixel nell'area locale in esecuzione nel passaggio di blocco. La formula esatta utilizzata per calcolare la sfumatura varia in base all'hardware, ma deve essere coerente con il modo in cui l'hardware esegue le stesse operazioni come parte del processo di calcolo del livello di dettaglio per il campionamento della trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[texldd-PS](texldd---ps.md)
</dt> </dl>

 

 




