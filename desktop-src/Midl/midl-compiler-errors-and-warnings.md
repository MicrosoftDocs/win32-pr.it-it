---
title: Errori e avvisi del compilatore MIDL
description: Quando si usa il compilatore MIDL, gli errori e gli avvisi possono essere causati da un uso non corretto delle opzioni della riga di comando o dal contenuto dei file IDL e ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language MIDL , informazioni di riferimento
- MIDL compiler MIDL , errors
- compilatore MIDL , errori
- errori MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f6c2dfd830a1240e2af107eb4a3f1799eafcd0de35ccec7f3756b3e9de5bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146404"
---
# <a name="midl-compiler-errors-and-warnings"></a>Errori e avvisi del compilatore MIDL

Quando si usa il compilatore MIDL, gli errori e gli avvisi possono essere causati da un uso non corretto delle opzioni della riga di comando o dal contenuto dei file IDL e ACF. Se l'errore è dovuto all'immissione non corretta delle opzioni della riga di comando, un messaggio di errore o di avviso può specificare il nome di una o più opzioni della modalità del compilatore MIDL. Ad esempio, è possibile includere determinati attributi ACF in un file IDL quando si usa l'opzione **/app \_ config,** ma tale file IDL genererà un errore se si esegue la compilazione senza usare l'opzione **/app \_ config.**

Gli errori nei file IDL e ACF rientrano in due categorie: errori rilevati dal preprocessore ed errori riconosciuti dal compilatore. Questa sezione elenca i messaggi di errore del compilatore e del preprocessore MIDL. Descrive anche i formati e le cause.

-   [Formati dei messaggi di errore e di avviso](error-and-warning-message-formats.md)
-   [Errori del preprocessore](preprocessor-errors.md)
-   [Errori del compilatore](compiler-errors.md)

 

 




