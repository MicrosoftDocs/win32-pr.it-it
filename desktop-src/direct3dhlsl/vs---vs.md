---
title: vs
description: Questa istruzione specifica il numero di versione dello shader. Questa istruzione funziona in tutte le versioni dello shader.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398292"
---
# <a name="vs"></a>vs

Questa istruzione specifica il numero di versione dello shader. Questa istruzione funziona in tutte le versioni dello shader.

## <a name="syntax"></a>Sintassi


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>Argomenti di input

Gli argomenti di input contengono un singolo numero di versione principale con un numero di versione secondario singolo. Le combinazioni consentite sono elencate nella tabella seguente.



| Versioni principali | Versioni secondarie                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0, SW (software), x (esteso) |
| 3             | 0, SW (software)               |



 

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

Questa istruzione deve essere la prima istruzione non di commento in un vertex shader.

Questa istruzione è supportata in tutte le versioni di vertex shader.

Le versioni con accelerazione hardware del software (versioni senza \_ SW nel numero di versione) possono elaborare i vertici con accelearation hardware o usare l'elaborazione dei vertici software. Le versioni del software (versioni con \_ SW nel numero di versione) elaborano i vertici solo con il software.

## <a name="examples"></a>Esempio

Questo esempio parziale dichiara un vertex shader della versione 1 \_ 1.


```
vs_1_1
```



Questo esempio parziale dichiara un vertex shader software della versione 2.


```
vs_2_sw
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




