---
title: phase - ps
description: L'istruzione di fase contrassegna la transizione tra la fase 1 e la fase 2. Se non è presente alcuna istruzione di fase, l'intero shader viene eseguito come se fosse uno shader di fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aac29792274a36ad4bb7266ffa02d0ea5d2bb1b6cec8efe2db213e9b0dd4890b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088694"
---
# <a name="phase---ps"></a>phase - ps

L'istruzione di fase contrassegna la transizione tra la fase 1 e la fase 2. Se non è presente alcuna istruzione di fase, l'intero shader viene eseguito come se fosse uno shader di fase 2.

Questa istruzione si applica solo alla versione \_ 1 4.

## <a name="syntax"></a>Sintassi


```
phase
```



## <a name="remarks"></a>Osservazioni



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| fase                 |      |      |      | x    |      |      |       |      |       |



 

Le istruzioni dello shader che si verificano prima dell'istruzione di fase sono istruzioni di fase 1. Tutte le altre istruzioni sono istruzioni della fase 2. Con due fasi per le istruzioni, viene aumentato il numero massimo di istruzioni per shader.

L'effetto collaterale negativo della transizione di fase è che il componente alfa dei [registri](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) temporanei non viene mantenuto durante la transizione. In altre parole, il componente alfa deve essere reinizializzato dopo l'istruzione di fase.

## <a name="example"></a>Esempio

Questo esempio illustra come raggruppare le istruzioni come istruzioni di fase 1 o fase 2 all'interno di uno shader.

L'istruzione di fase è anche comunemente chiamata marcatore di fase perché contrassegna la transizione tra le istruzioni di fase 1 e 2. In una versione 1 4 pixel shader, se il marcatore di fase non è presente, lo shader viene eseguito come se fosse \_ in esecuzione nella fase 2. Questo è importante perché esistono differenze tra le istruzioni di fase 1 e 2 e la disponibilità dei registri. Le differenze vengono notate in tutta la sezione di riferimento.


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




