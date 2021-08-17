---
title: Destinazione degli stub per piattaforme a 32 o 64 bit specifiche
description: Alcune delle funzionalità di Microsoft RPC e dei compilatori MIDL 3.0 e versioni successive sono specifiche della piattaforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- PIATTAFORME MIDL a 32 bit
- Piattaforme MIDL a 64 bit
- stub MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e0f78e47ed078bf7cd1fd78fa8730b597554a6c8ba1ed4fc5a67bc562e7d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641171"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Destinazione degli stub per piattaforme a 32 o 64 bit specifiche

Alcune delle funzionalità di Microsoft RPC e dei compilatori MIDL 3.0 e versioni successive sono specifiche della piattaforma.

Per precauzione, i compilatori MIDL 3.0 e versioni successive generano protezioni che facilitano il controllo di compatibilità durante la fase di compilazione C. MIDL genera due tipi di protezioni: una protezione dipendente dalla piattaforma (a 32 bit e a 64 bit) e una protezione dipendente dal rilascio (dipendenza del set di funzionalità). Ad esempio, MIDL genera la protezione seguente per impedire la compilazione C di uno stub a 32 bit per altre piattaforme:

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

La protezione dipendente dal rilascio viene attivata da un set di funzionalità presenti nei file IDL elaborati e [**dall'opzione /target.**](-target.md) Ad esempio, se l'interfaccia usa funzionalità supportate solo in Windows 2000 o versioni successive, MIDL genera una protezione con la macro TARGET \_ \_ IS NT50 \_ O VERSIONI \_ SUCCESSIVE.

Le macro guard, definite in Rpcndr.h, dipendono dall'impostazione di WINVER e WIN32 WINNT e vengono valutate dal compilatore \_ \_ C/C++.

Se, in fase di compilazione C, viene visualizzato un messaggio di errore che indica che è necessaria una piattaforma specifica per eseguire uno stub, verificare prima di tutto di non aver usato una funzionalità non disponibile in questa piattaforma. Le funzionalità che attivano una particolare protezione sono elencate nel corpo della protezione. Nell'esempio precedente l'opzione del compilatore -Oicf ha attivato la protezione. Funzionalità importanti di questo tipo includono l'opzione [**/robust**](-robust.md) e l'attributo \[ [**asincrono**](async.md) disponibili in Windows 2000 e versioni successive, il costruttore del tipo \] [**di pipe,**](pipe.md) l'opzione del compilatore /Oif e gli attributi di marshalling utente e wire \[ [**\_**](user-marshal.md) \] \[ [**\_ marshal.**](wire-marshal.md) \] Gli stub che usano queste funzionalità non verranno eseguiti nei sistemi precedenti.

Se si è a sapere che la piattaforma di destinazione è corretta per le funzionalità in uso e viene comunque visualizzato un errore, potrebbe essere necessario impostare le variabili di ambiente in modo appropriato.

**Per compilare per Windows 2000 o versioni successive**

-   Aggiungere questa riga al makefile:

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**/target**](-target.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**async**](async.md)
</dt> <dt>

[**async \_ uuid**](async-uuid.md)
</dt> <dt>

[**/oi**](-oi.md)
</dt> <dt>

[**inviare tramite pipe**](pipe.md)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> <dt>

[**marshalling \_ utente**](user-marshal.md)
</dt> <dt>

[Marshalling dei tipi di dati OLE](marshaling-ole-data-types.md)
</dt> </dl>

 

 




