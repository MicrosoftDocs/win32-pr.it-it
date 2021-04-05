---
title: Errori e avvisi del compilatore MIDL
description: Quando si usa il compilatore MIDL, errori e avvisi possono essere causati da un uso non corretto delle opzioni della riga di comando o dal contenuto dei file IDL e ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language MIDL, riferimento
- MIDL compilatore MIDL, errori
- MIDL del compilatore, errori
- errori MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855193"
---
# <a name="midl-compiler-errors-and-warnings"></a>Errori e avvisi del compilatore MIDL

Quando si usa il compilatore MIDL, errori e avvisi possono essere causati da un uso non corretto delle opzioni della riga di comando o dal contenuto dei file IDL e ACF. Se l'errore è dovuto all'immissione non corretta delle opzioni della riga di comando, un messaggio di errore o di avviso può specificare il nome di una o più opzioni della modalità del compilatore MIDL. Ad esempio, è possibile includere determinati attributi ACF in un file IDL quando si usa l'opzione **di \_ configurazione** di/app, ma il file IDL genererà un errore se si compila senza usare l'opzione di **\_ configurazione dell'app** /.

Gli errori nei file IDL e ACF rientrano in due categorie: errori rilevati dal preprocessore ed errori riconosciuti dal compilatore. Questa sezione elenca i messaggi di errore del compilatore e del preprocessore MIDL. Vengono inoltre descritti i formati e le cause.

-   [Formati di messaggio di errore e di avviso](error-and-warning-message-formats.md)
-   [Errori del preprocessore](preprocessor-errors.md)
-   [Errori del compilatore](compiler-errors.md)

 

 




