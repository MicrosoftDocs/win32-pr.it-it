---
title: LocalServer32
description: Specifica il percorso completo di un'applicazione server locale a 32 bit.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- LocalServer32 chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517164"
---
# <a name="localserver32"></a>LocalServer32

Specifica il percorso completo di un'applicazione server locale a 32 bit.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a>Commenti

Il valore **ServerExecutable** , che è di tipo **reg \_ SZ** ed è supportato a partire da Windows Server 2003, funziona insieme alla sottochiave **LocalServer32** per evitare ambiguità quando si usa la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . **LocalServer32** specifica il percorso dell'applicazione server COM da avviare e queste informazioni vengono passate come primo parametro *lpApplicationName* per **CreateProcess**. A seconda dell'implementazione di **CreateProcess**, le informazioni potrebbero essere ambigue. Per questo motivo, se si specifica **ServerExecutable** , com passa il valore **ServerExecutable** denominato al parametro *lpApplicationName* di **CreateProcess**. Se **ServerExecutable** viene omesso, com passa **null** come valore per il primo parametro di **CreateProcess**.

Per fornire la sicurezza del sistema, usare stringhe tra virgolette nel percorso per indicare dove termina il nome file eseguibile e gli argomenti iniziano. Ad esempio, anziché specificare il percorso seguente come voce **LocalServer32** :

"C: \\ programmi \\ aziendali file \\Application.exe param1 param2"

specificare il percorso usando la sintassi seguente:

" \\ " C: \\ programmi \\ aziendali file \\Application.exe\\ "param1 param2"

COM aggiunge il flag "-Embedding" alla stringa, quindi l'applicazione che usa i flag deve analizzare l'intera stringa e verificare la presenza del flag-Embedding.

Quando COM avvia un server locale a 32 bit, il server deve registrare un oggetto classe entro un tempo trascorso impostato dall'utente. Per impostazione predefinita, il valore del tempo trascorso deve essere almeno di 5 minuti, in millisecondi, ma non può superare il numero di millisecondi in 30 giorni. Le applicazioni in genere non devono impostare questo valore, che si trova nella voce **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ COM2 \\ ServerStartElapsedTime**

Le voci obbligatorie per i server locali a 32 bit sono [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** e [**Insertable**](insertable.md).

Se un contenitore esegue la ricerca nel registro di sistema per un server locale, un server locale a 32 bit ha la priorità su un server locale a 16 bit.

Se si implementano classi come servizi, è necessario tenere presente che il valore denominato [**LocalService**](localservice.md) viene usato in preferenza con la chiave **LocalServer32** per l'attivazione locale e remota Requestsâ € "Se **LocalService** esiste e fa riferimento a un servizio valido, la chiave **LocalServer32** viene ignorata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**LocalServer**](localserver.md)
</dt> <dt>

[**LocalService**](localservice.md)
</dt> </dl>

 

 