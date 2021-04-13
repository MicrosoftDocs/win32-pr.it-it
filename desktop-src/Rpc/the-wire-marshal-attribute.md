---
title: Attributo wire_marshal
description: L'attributo \ Wire \_ Marshal \ è un attributo di tipo IDL simile alla sintassi di \ trasmette \_ come \, ma fornisce un modo più efficiente per effettuare il marshalling dei dati in una rete.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- RPC, attributi, wire_marshal di procedura remota
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399420"
---
# <a name="the-wire_marshal-attribute"></a>Attributo Wire \_ Marshal

L' \[ attributo [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] è un attributo di tipo IDL simile alla sintassi per la \[ [trasmissione \_ come](/windows/desktop/Midl/transmit-as) \] , ma fornisce un modo più efficiente per eseguire il marshalling dei dati in una rete.

L' \[ attributo **Wire \_ Marshal** viene utilizzato \] per specificare un tipo di dati che verrà trasmesso al posto del tipo di dati specifico dell'applicazione. Ogni tipo specifico dell'applicazione ha un tipo transmittable corrispondente che definisce la rappresentazione in transito (la rappresentazione utilizzata sulla rete). Il tipo specifico dell'applicazione non deve essere transmittable, ma deve essere un tipo riconosciuto da MIDL. Per effettuare il marshalling di un tipo sconosciuto a MIDL, usare il \[ [ \_ marshalling utente](/windows/desktop/Midl/user-marshal)dell'attributo ACF \] .

Il tipo specifico dell'applicazione può essere un tipo semplice, composto o puntatore. La restrizione principale è che l'istanza del tipo deve avere una dimensione di memoria fissa e ben definita. Se è necessario modificare le dimensioni dell'istanza del tipo, utilizzare un campo puntatore anziché una matrice conforme. In alternativa, è possibile definire un puntatore al tipo modificabile.

È necessario fornire le routine per il ridimensionamento, il marshalling e l'unmarshalling dei dati, oltre a liberare la memoria associata. Nella tabella seguente vengono descritti i quattro nomi di routine specificati dall'utente. <type>È il tipo utente specificato nella definizione del tipo di \[ **\_ marshalling di rete** \] .



| Routine                                                            | Descrizione                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_UserSize](the-type-usersize-function.md)           | Ridimensiona il buffer di dati RPC prima del marshalling sul lato client o server. |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | Esegue il marshalling dei dati sul lato client o server.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Esegue l'unmarshalling dei dati sul lato client o server.                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | Libera i dati sul lato server.                                        |



 

Queste routine fornite dal programmatore vengono fornite dal client o dall'applicazione server basata sugli attributi direzionali.

Se il parametro è \[ solo [in](/windows/desktop/Midl/in) \] , il client trasmette al server. Il client richiede le funzioni **<type> \_ UserSize** e **<type> \_ UserMarshal** . Per il server sono necessarie le funzioni **<type> \_ UserUnmarshal** e **<type> \_ UserFree** .

Per un \[ [](/windows/desktop/Midl/out-idl) \] parametro di sola uscita, il server trasmette al client. Il server necessita delle funzioni **<type> \_ UserSize** e **<type> \_ UserMarshal** , mentre il client richiede la funzione **<type> \_ UserMarshal** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Attributo Marshal utente](the-user-marshal-attribute.md)
</dt> <dt>

[Regole di marshalling per \_ marshalling utente e \_ marshalling di rete](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshalling di rete](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_marshalling utente](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 