---
title: output dcl_usage (SM1, SM2, SM3-vs ASM)
description: I vari tipi di registri di output sono stati compressi in dodici registri di output (due per colore, otto per trama, uno per la posizione e uno per la nebbia e la dimensione del punto).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993525"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>\_output utilizzo DCL (SM1, SM2, SM3-vs ASM)

I vari tipi di registri di output sono stati compressi in dodici registri di output (due per colore, otto per trama, uno per la posizione e uno per la nebbia e la dimensione del punto). Questi possono essere usati per qualsiasi elemento che l'utente vuole interpolare per il pixel shader: coordinate di trama, colori, nebbia e così via.

I registri di output richiedono dichiarazioni che includono la semantica. Ad esempio, i registri della posizione precedente e delle dimensioni dei punti vengono sostituiti dichiarando un registro di output con una posizione o una semantica delle dimensioni del punto.

Dei dodici registri di output, le dieci (non necessariamente o0 a O9) hanno quattro componenti (xyzw), un altro deve essere dichiarato come position (e deve includere anche tutti e quattro i componenti) e, facoltativamente, un altro può essere una dimensione scalare.

## <a name="syntax"></a>Sintassi

La sintassi per la dichiarazione dei registri di output è simile a quella per il registro di input:



|                                  |
|----------------------------------|
| \_maschera di semantica DCL o \[ . Write \_\] |



 

Dove:

-   \_la semantica di DCL può utilizzare lo stesso set di semantica della dichiarazione di input. I nomi semantici provengono da [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (e sono associati a un indice, ad esempio POSITION3). Quando non viene usato per l'elaborazione dei vertici, deve essere sempre presente un registro di output con la semantica positiont0. La semantica positiont0 e la semantica pointsize0 sono le uniche che hanno un significato superiore a quello che consente semplicemente il collegamento da vertex a pixel shader. Per gli shader con il controllo di flusso, si presuppone che l'output del case peggiore venga dichiarato. Non esistono valori predefiniti se uno shader non genera effettivamente il risultato che dichiara, a causa del controllo di flusso.
-   o è un registro di output. Vedere [ \_ registri di output](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).
-   Write \_ mask indica lo stesso registro di output che può essere dichiarato più volte, in modo che sia possibile applicare una semantica diversa a singoli componenti, ogni volta con una maschera di scrittura univoca. Tuttavia, la stessa semantica non può essere utilizzata più volte in una dichiarazione. Ciò significa che i vettori devono essere costituiti da quattro componenti o meno e non possono superare i limiti di registro a quattro componenti (registri singoli). Quando si usa la semantica delle dimensioni del punto, deve avere una maschera di scrittura completa perché è considerata scalare. Quando si usa la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti devono essere scritti.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 3 \_ 0 | 3 \_ SW |
|------------------------|------|-------|
| utilizzo di DCL \_             | x    | x     |



 

Tutte le istruzioni di [ \_ utilizzo di DCL](dcl-usage-input-register---vs.md) devono essere visualizzate prima della prima istruzione eseguibile.

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

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 