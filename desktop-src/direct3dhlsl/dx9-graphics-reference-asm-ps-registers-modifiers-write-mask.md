---
title: Maschera di scrittura registro di destinazione
description: Una maschera di scrittura controlla i componenti di un registro di destinazione che vengono scritti dopo il completamento di un'istruzione.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955839"
---
# <a name="destination-register-write-mask"></a>Maschera di scrittura registro di destinazione

Una maschera di scrittura controlla i componenti di un registro di destinazione che vengono scritti dopo il completamento di un'istruzione. È consentita una maschera di scrittura di output purché i componenti si trovino nell'ordine di. RGBA o. xyzw. Ovvero. RBA e. XW sono maschere valide. I registri di trama includono un set di regole e registri non di trama hanno un altro set di regole.

## <a name="syntax"></a>Sintassi



| DST. writemask |
|---------------|



 

dove

-   DST è un registro di destinazione.
-   writemask è una sequenza di maschere da entrambi i set: (x, y, z, w) o (rosso, verde, blu, alfa).

## <a name="remarks"></a>Commenti

Sono disponibili le seguenti maschere di scrittura di destinazione.



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| . xyzw (impostazione predefinita)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . xyz                  | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| maschera arbitraria        |      |      |      | x    | x    | x    | x     | x    | x     |



 

La maschera arbitraria consente di combinare qualsiasi set di canali per produrre una maschera. I canali devono essere elencati nell'ordine r, g, b, a, ad esempio Register. RBA, che aggiorna i canali rosso, blu e alfa della destinazione. La maschera arbitraria è disponibile nella versione 1 \_ 4 o successiva.

Se non viene specificata alcuna maschera di scrittura di destinazione, per impostazione predefinita viene applicata la maschera di scrittura di destinazione al case RGBA. In altre parole, vengono aggiornati tutti i canali nel registro di destinazione.

Per le versioni \_ da 1 0 a 1 \_ 3, l'istruzione aritmetica [DP3-PS](dp3---ps.md) DP3 può usare solo le maschere di scrittura dell'output con estensione RGB o RGBA.

Le maschere di scrittura del registro di destinazione sono supportate solo per operazioni aritmetiche. Non possono essere usati nelle istruzioni per l'indirizzamento delle trame, fatta eccezione per le istruzioni della versione 1 \_ 4, [texcrd-PS](texcrd---ps.md) e [texld-PS \_ 2 \_ 0](texld---ps-2-0.md).

Per impostazione predefinita, vengono scritti tutti e quattro i canali colori.


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



La maschera di scrittura alfa è detta anche maschera di scrittura scalare, perché usa la pipeline scalare.


```
add r0.a, t1, v1
```



Quindi, questa istruzione inserisce in modo efficace la somma del componente alfa di T1 e del componente alfa di V1 in r0. a.

La maschera di scrittura colori viene utilizzata per controllare la scrittura nei canali dei colori.


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



Per la versione 1 \_ 4, le maschere di scrittura di destinazione possono essere usate in qualsiasi combinazione purché le maschere siano ordinate come r, g, b, a.


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



Un'istruzione co-emesso consente di emettere due istruzioni potenzialmente diverse contemporaneamente. Questa operazione viene eseguita eseguendo le istruzioni della pipeline Alpha e della pipeline RGB.


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



Il vantaggio di abbinare le istruzioni in questo modo è che consente di eseguire diverse operazioni nella pipeline vettoriale e scalare in parallelo.

Questi registri di output del vertex shader sono limitati alle seguenti maschere di scrittura:



| Tipo di registro | Maschera di scrittura obbligatoria                                              |
|---------------|------------------------------------------------------------------|
| oFog          | Nessuna maschera di scrittura esplicita consentita in questo registro scalare        |
| oPts          | Nessuna maschera di scrittura esplicita consentita in questo registro scalare        |
| oPos          | . xyzw (impostazione predefinita)                                      |
| oT\#          | maschera combinata:. x \| . XY \| . xyz \| . xyzw (impostazione predefinita) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




