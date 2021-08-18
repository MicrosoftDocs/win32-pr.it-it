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
ms.openlocfilehash: 3977e77c685adb3a181804c0db5b281ae3e54c6f085586023855259f532dde8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484231"
---
# <a name="vs"></a>vs

Questa istruzione specifica il numero di versione dello shader. Questa istruzione funziona in tutte le versioni dello shader.

## <a name="syntax"></a>Sintassi


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a>Argomenti di input

Gli argomenti di input contengono un singolo numero di versione principale con un singolo numero di versione secondario. Le combinazioni consentite sono elencate nella tabella seguente.



| Versioni principali | Versioni secondarie                   |
|---------------|--------------------------------|
| 1             | 1                              |
| 2             | 0, sw (software), x (esteso) |
| 3             | 0, sw (software)               |



 

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| vs                     | x    | x    | x    | x     | x    | x     |



 

Questa istruzione deve essere la prima istruzione non di commento in un vertex shader.

Questa istruzione è supportata in tutte le versioni di vertex shader.

Le versioni con accelerazione hardware del software (versioni senza sw nel numero di versione), possono elaborare i vertici con \_ l'accelearazione hardware o usare l'elaborazione dei vertici software. Le versioni software (versioni \_ con sw nel numero di versione) elaborano i vertici solo con il software.

## <a name="examples"></a>Esempio

Questo esempio parziale dichiara un vertex shader versione \_ 1 1.


```
vs_1_1
```



Questo esempio parziale dichiara un vertex shader software versione 2.


```
vs_2_sw
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




