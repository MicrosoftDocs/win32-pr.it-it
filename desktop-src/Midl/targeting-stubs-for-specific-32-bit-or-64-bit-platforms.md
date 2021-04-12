---
title: Destinazione degli stub per piattaforme specifiche a 32 bit o a 64 bit
description: Alcune delle funzionalità di Microsoft RPC e i compilatori MIDL 3,0 e versioni successive sono specifici della piattaforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- piattaforme a 32 bit MIDL
- piattaforme a 64 bit MIDL
- Stub MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331380"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Destinazione degli stub per piattaforme specifiche a 32 bit o a 64 bit

Alcune delle funzionalità di Microsoft RPC e i compilatori MIDL 3,0 e versioni successive sono specifici della piattaforma.

Per precauzione, i compilatori MIDL 3,0 e versioni successive generano protezioni che facilitano il controllo della compatibilità durante la fase di compilazione C. MIDL genera due tipi di protezioni: un GUARD dipendente dalla piattaforma (32 bit rispetto a 64 bit) e un GUARD dipendente dalla versione (dipendenza dal set di funzionalità). Ad esempio, MIDL genera la seguente protezione per impedire la compilazione C di uno stub a 32 bit per altre piattaforme:

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

Il Guard dipendente dalla versione viene attivato da un set di funzionalità trovate nei file IDL elaborati e dall'opzione [**/target**](-target.md) . Se, ad esempio, l'interfaccia usa funzionalità supportate solo in Windows 2000 o versioni successive, MIDL genera una protezione con la destinazione \_ è \_ NT50 \_ o una \_ macro successiva.

Le macro Guard, definite in Rpcndr. h, dipendono dall'impostazione di WINVER e \_ Win32 \_ WinNT e vengono valutate dal compilatore C/C++.

Se, in fase di compilazione C, viene ricevuto un messaggio di errore che indica che è necessaria una piattaforma specifica per eseguire uno stub, verificare prima di tutto che non sia stata usata una funzionalità non disponibile in questa piattaforma. Le funzionalità che attivano una particolare protezione sono elencate nel corpo della protezione. Nell'esempio precedente, l'opzione del compilatore-Oicf ha attivato la protezione. Le funzionalità rilevanti di questo tipo includono l'opzione [**/robust**](-robust.md) e l' \[ [](async.md) \] attributo asincrono disponibile in Windows 2000 e versioni successive, il costruttore del tipo di [**pipe**](pipe.md) , l'opzione del compilatore/OIF e gli attributi di \[ [**\_ marshalling degli utenti**](user-marshal.md) \] e del \[ [**\_ marshalling di rete**](wire-marshal.md) \] . Gli stub che usano queste funzionalità non vengono eseguiti nei sistemi precedenti.

Se si è certi che la piattaforma di destinazione è corretta per le funzionalità in uso e viene comunque visualizzato un errore, potrebbe essere necessario impostare le variabili di ambiente in modo appropriato.

**Per compilare per Windows 2000 o versioni successive**

-   Aggiungere questa riga al Makefile:

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**/target**](-target.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**async**](async.md)
</dt> <dt>

[**\_UUID asincrono**](async-uuid.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**inviare tramite pipe**](pipe.md)
</dt> <dt>

[**\_marshalling di rete**](wire-marshal.md)
</dt> <dt>

[**\_marshalling utente**](user-marshal.md)
</dt> <dt>

[Marshalling di tipi di dati OLE](marshaling-ole-data-types.md)
</dt> </dl>

 

 




