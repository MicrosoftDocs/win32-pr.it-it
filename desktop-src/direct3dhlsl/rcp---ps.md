---
title: rcp - ps
description: Calcola il reciproco dello scalare di origine. | rcp - ps
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fba443d4a2e05794f8c1965e46a61c65edae50b95845f0f80faa0c0ab6c6bf71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510956"
---
# <a name="rcp---ps"></a>rcp - ps

Calcola il reciproco dello scalare di origine.

## <a name="syntax"></a>Sintassi



| rcp dst, src |
|--------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito di replicate swizzle, ovvero esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalenti) deve essere specificato.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rcp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

L'output deve essere esattamente 1.0 se l'input è esattamente 1.0. Un'origine 0,0 restituisce infinito.

Il risultato scalare viene replicato in tutti i canali nella maschera di scrittura di destinazione.

La precisione deve essere almeno 1,0/(2²²) errore assoluto nell'intervallo (1.0, 2.0) perché le implementazioni comuni separeranno mantissa ed esponente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




