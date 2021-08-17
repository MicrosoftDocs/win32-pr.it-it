---
title: dcl_usage output (sm1, sm2, sm3 - vs asm)
description: I vari tipi di registri di output sono stati compressi in dodici registri di output (due per il colore, otto per la trama, uno per la posizione e uno per le dimensioni dei punti e dei punti).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee5f444cbf145957ad93db00160d812e75e4a624019ad9f578b5dc960e84f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726718"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>Output dcl \_ usage (sm1, sm2, sm3 - vs asm)

I vari tipi di registri di output sono stati compressi in dodici registri di output (due per il colore, otto per la trama, uno per la posizione e uno per le dimensioni dei punti e dei punti). Possono essere usati per qualsiasi elemento che l'utente vuole interpolare per il pixel shader: coordinate della trama, colori, blu e così via.

I registri di output richiedono dichiarazioni che includono semantica. Ad esempio, la posizione precedente e i registri delle dimensioni dei punti vengono sostituiti dichiarando un registro di output con una semantica di posizione o dimensione del punto.

Dei dodici registri di output, ogni dieci (non necessariamente o0 a o9) ha quattro componenti (xyzw), un altro deve essere dichiarato come position (e deve includere anche tutti e quattro i componenti) e, facoltativamente, uno di più può essere una dimensione in punti scalari.

## <a name="syntax"></a>Sintassi

La sintassi per la dichiarazione dei registri di output è simile alle dichiarazioni per il registro di input:



|                                  |
|----------------------------------|
| dcl \_ semantics o \[ .write \_ mask\] |



 

Dove:

-   La semantica dcl \_ può usare lo stesso set di semantica della dichiarazione di input. I nomi semantici [**provengono da D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (e sono associati a un indice, ad esempio position3). Deve essere sempre presente un registro di output con la semantica positiont0 quando non viene usato per l'elaborazione dei vertici. La semantica positiont0 e la semantica pointsize0 sono gli unici che hanno significato oltre a consentire semplicemente il collegamento da vertex shader a pixel shader. Per gli shader con controllo di flusso, si presuppone che l'output del caso peggiore sia dichiarato. Non sono presenti impostazioni predefinite se uno shader non restituisce effettivamente l'output che dovrebbe (a causa del controllo di flusso).
-   o è un registro di output. Vedere [Registri \_ di output.](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)
-   write mask indica lo stesso registro di output che può essere dichiarato più volte (in modo che sia possibile applicare una semantica diversa ai singoli componenti), ogni volta con \_ una maschera di scrittura univoca. Tuttavia, la stessa semantica non può essere usata più volte in una dichiarazione. Ciò significa che i vettori devono essere quattro o meno componenti e non possono attraversare i limiti del registro a quattro componenti (singoli registri). Quando viene usata la semantica delle dimensioni del punto, deve avere una maschera di scrittura completa perché è considerata scalare. Quando viene usata la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti devono essere scritti.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 3 \_ 0 | 3 \_ sw |
|------------------------|------|-------|
| dcl \_ usage             | x    | x     |



 

Tutte [le istruzioni dcl \_ usage](dcl-usage-input-register---vs.md) devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="declaration-examples"></a>Esempi di dichiarazione


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
