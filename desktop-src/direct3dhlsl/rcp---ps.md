---
title: RCP-PS
description: Calcola il reciproco del valore scalare di origine. | RCP-PS
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981730"
---
# <a name="rcp---ps"></a>RCP-PS

Calcola il reciproco del valore scalare di origine.

## <a name="syntax"></a>Sintassi



| RCP DST, src |
|--------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rcp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

L'output deve essere esattamente 1,0 se l'input è esattamente 1,0. Un'origine di 0,0 restituisce un valore infinito.

Il risultato scalare viene replicato in tutti i canali nella maschera di scrittura di destinazione.

La precisione deve essere un errore assoluto di almeno 1,0/(2 ² ²) nell'intervallo (1,0, 2,0) perché le implementazioni comuni separano mantissa ed esponente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




