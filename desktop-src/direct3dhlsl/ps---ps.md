---
title: ps
description: Questa istruzione specifica il numero di versione dello shader e funziona in tutte le versioni dello shader.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993192"
---
# <a name="ps"></a>ps

Questa istruzione specifica il numero di versione dello shader e funziona in tutte le versioni dello shader.

## <a name="syntax"></a>Sintassi


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a>Argomenti di input

Gli argomenti di input contengono un singolo numero di versione principale con un numero di versione secondario singolo. Le combinazioni consentite sono elencate nella tabella seguente.



| Versioni principali | Versioni secondarie                   |
|---------------|--------------------------------|
| 1             | 1, 2, 3, 4                     |
| 2             | 0, x (esteso), SW (software) |
| 3             | 0, SW (software)               |



 

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ps                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Questa istruzione deve essere la prima istruzione non di commento in una pixel shader.

Le versioni con accelerazione hardware del software (versioni senza \_ SW nel numero di versione) possono elaborare i vertici con accelearation hardware o usare l'elaborazione dei vertici software. Le versioni del software (versioni con \_ SW nel numero di versione) elaborano i vertici solo con il software.

## <a name="examples"></a>Esempio

In questo esempio parziale viene dichiarata una versione 1 \_ 1 pixel shader.


```
ps_1_1
```



Questo esempio parziale dichiara una versione 1 \_ 4 pixel shader.


```
ps_1_4
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




