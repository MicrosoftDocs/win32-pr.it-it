---
title: fase-PS
description: L'istruzione Phase contrassegna la transizione tra la fase 1 e la fase 2. Se non è presente alcuna istruzione della fase, l'intero shader viene eseguito come se fosse uno shader della fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046113"
---
# <a name="phase---ps"></a>fase-PS

L'istruzione Phase contrassegna la transizione tra la fase 1 e la fase 2. Se non è presente alcuna istruzione della fase, l'intero shader viene eseguito come se fosse uno shader della fase 2.

Questa istruzione si applica solo alla versione 1 \_ 4.

## <a name="syntax"></a>Sintassi


```
phase
```



## <a name="remarks"></a>Osservazioni



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| fase                 |      |      |      | x    |      |      |       |      |       |



 

Le istruzioni dello shader che si verificano prima dell'istruzione Phase sono le istruzioni della fase 1. Tutte le altre istruzioni sono le istruzioni della fase 2. Con due fasi per le istruzioni, viene aumentato il numero massimo di istruzioni per shader.

Lo sfortunato effetto collaterale della transizione della fase è che il componente alfa dei [registri temporanei](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) non viene mantenuto durante la transizione. In altre parole, è necessario reinizializzare il componente alfa dopo l'istruzione Phase.

## <a name="example"></a>Esempio

Questo esempio illustra come raggruppare le istruzioni come fase 1 o le istruzioni della fase 2 in uno shader.

L'istruzione Phase viene comunemente chiamata marcatore fase perché contrassegna la transizione tra le istruzioni Phase 1 e 2. In una versione 1 \_ 4 pixel shader, se il marcatore di fase non è presente, lo shader viene eseguito come se fosse in esecuzione nella fase 2. Questo aspetto è importante perché esistono differenze tra le istruzioni Phase 1 e 2 e la disponibilità del registro. Le differenze sono indicate nella sezione di riferimento.


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




