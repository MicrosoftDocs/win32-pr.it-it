---
title: Modificatori del registro di origine vertex shader
description: I modificatori di origine possono essere applicati per modificare i dati letti da un registro di origine prima che i dati vengano utilizzati dall'istruzione.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396403"
---
# <a name="vertex-shader-source-register-modifiers"></a>Modificatori del registro di origine vertex shader

I modificatori di origine possono essere applicati per modificare i dati letti da un registro di origine prima che i dati vengano utilizzati dall'istruzione.

## <a name="negate"></a>Negate

Negare il contenuto del registro di origine.



| Modificatore Component | Descrizione     |
|--------------------|-----------------|
| \- r               | Negazione origine |



 

Non è possibile usare il modificatore negazioni nel secondo registro di origine di queste istruzioni: [M3X2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [M4x4-vs](m4x4---vs.md).



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Valore assoluto

Assumere il valore assoluto del registro.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Se una versione 3 dello shader legge da uno o più registri float costanti (c \# ), uno dei seguenti deve essere true.

-   Tutti i registri a virgola mobile costanti devono usare il modificatore ABS.
-   Nessun registro a virgola mobile costante può utilizzare il modificatore ABS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




