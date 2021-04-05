---
title: Protezione del buffer MCCP
description: A partire da Windows Vista, il motore di marshalling RPC esegue ulteriori passaggi per evitare sovraccarichi del buffer sul lato client a causa dei dati restituiti. Questa funzionalità è detta protezione della conformità di calcolo minima (MCCP).
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d04de57974bd9665d659129590d72513eb83e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729799"
---
# <a name="mccp-buffer-protection"></a>Protezione del buffer MCCP

A partire da Windows Vista, il motore di marshalling RPC esegue ulteriori passaggi per evitare sovraccarichi del buffer sul lato client a causa dei dati restituiti. Questa funzionalità è detta protezione della conformità di calcolo minima (MCCP).

Quando il client passa un puntatore a un buffer esistente a un \[ parametro [**out**](/windows/desktop/Midl/out-idl) \] o \[ [**in**](/windows/desktop/Midl/in)**out** \] , i dati restituiti per il parametro vengono copiati nel buffer esistente. Se i dati restituiti sono maggiori del buffer passato, può verificarsi un sovraccarico del buffer quando RPC copia i dati restituiti nel buffer troppo piccolo. Vedere [puntatori di primo livello e incorporati](top-level-and-embedded-pointers.md).

Con MCCP, RPC tenta di rilevare questa condizione e di rifiutare la chiamata se viene rilevata. Per i buffer con un valore di correlazione, ad esempio \[ [**size \_**](/windows/desktop/Midl/size-is) \] , se i dati restituiti non rientrano nella dimensione del buffer specificata, la chiamata viene rifiutata e \_ \_ viene generata l'eccezione RPC X Bad \_ Stub \_ Data. Per le stringhe non dimensionate, la chiamata viene rifiutata se la dimensione della stringa esistente (lunghezza fino al carattere di terminazione **null** ) non è sufficiente per conservare la stringa restituita, la chiamata viene rifiutata. RPC non è in grado di rilevare i sovraccarichi del buffer in tutte le condizioni, quindi lo sviluppatore deve continuare a adottare le normali precauzioni per i sovraccarichi del buffer.

Se il client non passa un buffer esistente per un parametro \[ [**out**](/windows/desktop/Midl/out-idl) \] , ma passa invece un puntatore dereferenziato a **null**, RPC seguirà le normali regole per allocare un nuovo buffer per conto del client. Questo buffer verrà allocato con spazio sufficiente per contenere i dati restituiti.

Una seconda protezione è che, per i parametri correlati, RPC imporrà che viene passato un buffer non **null** quando la variabile di conteggio delle correlazioni è non **null**.

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

Se la *stringa* è **null**, RPC rifiuterà la chiamata a meno che *length* non sia impostato su 0. Si noti che RPC consentirà la *lunghezza* pari a 0 mentre la *stringa* è non **null** e RPC tratterà la *stringa* come un'allocazione di buffer di lunghezza 0.

 

 