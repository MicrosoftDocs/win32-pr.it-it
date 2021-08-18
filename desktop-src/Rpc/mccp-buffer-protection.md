---
title: Protezione buffer MCCP
description: A partire Windows Vista, il motore di marshalling RPC esegue altri passaggi per tentare di evitare sovraccarichi del buffer lato client a causa dei dati restituiti. Questa funzionalità è denominata Mini Compute Conformance Protection (MCCP).
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b95234eed76c3d8f0fdc34b0b53e9cf02bcae2fd6db62694e1a3aadd602076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928407"
---
# <a name="mccp-buffer-protection"></a>Protezione buffer MCCP

A partire Windows Vista, il motore di marshalling RPC esegue altri passaggi per tentare di evitare sovraccarichi del buffer lato client a causa dei dati restituiti. Questa funzionalità è denominata Mini Compute Conformance Protection (MCCP).

Quando il client passa un puntatore a un buffer esistente a un parametro out o out, i dati restituiti per tale parametro vengono \[ [](/windows/desktop/Midl/out-idl) \] \[ [](/windows/desktop/Midl/in) \] copiati nel buffer esistente. Se i dati restituiti sono più grandi del buffer passato, è possibile che si verifichi un sovraccarico del buffer quando RPC copia i dati restituiti nel buffer troppo piccolo. Vedere [Puntatori incorporati e di primo livello.](top-level-and-embedded-pointers.md)

Con MCCP, RPC tenta di rilevare questa condizione e rifiutare la chiamata se rilevata. Per i buffer con un valore di correlazione, ad esempio size è , se i dati restituiti non rientrano nelle dimensioni del buffer specificate, la chiamata viene rifiutata e viene generata l'eccezione \[ [**\_**](/windows/desktop/Midl/size-is) \] STUB DATA RPC \_ X \_ \_ \_ BAD. Per le stringhe non ridimensionate, la chiamata viene rifiutata se le dimensioni della stringa esistente (lunghezza fino al terminatore **Null)** non sono sufficienti per contenere la stringa restituita, la chiamata viene rifiutata. RPC non è in grado di rilevare i sovraccarichi del buffer in tutte le condizioni, pertanto è consigliabile che lo sviluppatore continui a adottare precauzioni normali contro i sovraccarichi del buffer.

Se il client non passa un buffer esistente per un parametro out, ma passa invece un puntatore dereferenziato \[ [](/windows/desktop/Midl/out-idl) \] a **NULL,** RPC seguirà le normali regole per allocare un nuovo buffer per conto del client. Questo buffer verrà allocato con spazio sufficiente per contenere i dati restituiti.

Una seconda protezione è che per i parametri correlati, RPC imposirà che viene passato un buffer non **Null** quando la variabile di conteggio delle correlazioni è non **Null.**

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

Se *MyString* è **NULL,** RPC rifiuterà la chiamata a meno *che Length* non sia impostato su 0. Si noti che RPC consentirà *a Length* di essere 0 mentre *MyString* è diverso da **NULL** e RPC tratterà *MyString* come un'allocazione di buffer di lunghezza 0.

 

 