---
title: Funzione type_UserMarshal
description: La funzione \_ UserMarshal di tipo è una funzione helper per gli attributi \wire \_ marshal\ e \user \_ marshal\.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42bd7ce6d9d107fe24affc895ba802e73ee8fe0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880897"
---
# <a name="the-type_usermarshal-function"></a>Funzione \_ UserMarshal di tipo

La **&lt; funzione &gt; \_ UserMarshal di tipo** è una funzione helper per gli attributi wire \[ [ \_ marshal](/windows/desktop/Midl/wire-marshal) \] e user \[ [ \_ marshal.](/windows/desktop/Midl/user-marshal) \] Gli stub chiamano questa funzione per effettuare il marshalling dei dati sul lato client o server. La funzione è definita come:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

Il tipo nel nome della funzione indica il tipo userm specificato nella definizione del tipo wire &lt; &gt; **\[ \_ marshal \]** o **\[ user \_ marshal. \]** Questo tipo può essere non ritrasmettibile o persino, se usato con l'attributo **\[ \_ di marshalling \]** dell'utente, un tipo sconosciuto al compilatore MIDL. Il nome del tipo di collegamento (il nome del tipo trasmissibile) non viene usato nel prototipo di funzione. Si noti, tuttavia, che il tipo wire definisce il layout di collegamento per i dati come specificato da OSF DCE.

Il *parametro pFlags* è un puntatore a un campo di flag long senza segno. La parola superiore del flag contiene flag di rappresentazione dei dati NDR come definito da DCE OSF per le rappresentazioni a virgola mobile, ordine dei byte e caratteri. La parola inferiore contiene un flag di contesto di marshalling come definito dal canale COM. Il layout esatto dei flag all'interno del campo è descritto in [Funzione \_ UserSize di tipo](the-type-usersize-function.md).

Il *parametro pBuffer* è il puntatore del buffer corrente. Questo puntatore può essere allineato o meno alla voce. La **&lt; funzione &gt; \_ UserMarshal di** tipo deve allineare il puntatore del buffer in modo appropriato, effettuare il marshalling dei dati e restituire la nuova posizione del buffer, ovvero l'indirizzo del primo byte dopo l'oggetto sottoposto a marshalling. Tenere presente che la specifica del tipo di collegamento determina il layout effettivo dei dati nel buffer.

Il *parametro pMyObj* è un puntatore a un oggetto di tipo utente.

Il valore restituito è la nuova posizione del buffer, ovvero l'indirizzo del primo byte dopo l'oggetto di cui non è stato reso disponibile ilmarshaled.

L'overflow del buffer può verificarsi quando si calcolano in modo non corretto le dimensioni dei dati e si tenta di effettuare il marshalling di più dati del previsto. È necessario prestare attenzione a evitare questa situazione. È possibile eseguire una verifica usando il puntatore **&lt; restituito &gt; \_ da UserMarshal.** In caso contrario, si rischia che il motore NDR genererà un'eccezione di overflow del buffer in un secondo momento.

Le eccezioni devono essere intercettate e gestite in locale, le eccezioni non devono essere autorizzate a propiziare lo stack di chiamate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Regole di marshalling per il marshalling \_ dell'utente e il wire \_ marshal](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[marshalling \_ utente](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 
