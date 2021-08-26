---
title: Modificatori del registro di origine vertex shader
description: I modificatori di origine possono essere applicati per modificare i dati letti da un registro di origine prima che i dati siano usati dall'istruzione .
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f50942d32691d9dc76aa30ddcef36df390fccfe058c31af3527c0eafe0d7df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067981"
---
# <a name="vertex-shader-source-register-modifiers"></a>Modificatori del registro di origine vertex shader

I modificatori di origine possono essere applicati per modificare i dati letti da un registro di origine prima che i dati siano usati dall'istruzione .

## <a name="negate"></a>Negate

Negare il contenuto del registro di origine.



| Modificatore di componente | Descrizione     |
|--------------------|-----------------|
| \- R               | Negazione dell'origine |



 

Il modificatore negazione non può essere usato nel secondo registro di origine di queste istruzioni: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs , m4x4 - vs](m4x4---vs.md).



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Valore assoluto

Prendere il valore assoluto del registro.



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Se uno shader versione 3 legge da uno o più registri float costanti (c), uno dei \# seguenti deve essere true.

-   Tutti i registri a virgola mobile costanti devono usare il modificatore abs.
-   Nessuno dei registri a virgola mobile costanti può usare il modificatore abs.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




