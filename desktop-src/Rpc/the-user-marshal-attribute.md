---
title: Attributo user_marshal
description: L'attributo \ user \_ marshal\ è un attributo di tipo ACF simile nella sintassi a \ represent \_ as\ .
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- RPC Remote Procedure Call , attributi e user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0501cfd3199d41a49da7f54919c86f9332ce976f33963f23c63a7938338da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923531"
---
# <a name="the-user_marshal-attribute"></a>Attributo \_ marshalling utente

\[ [L'attributo di \_ marshalling](/windows/desktop/Midl/user-marshal) \] utente è un attributo di tipo ACF simile nella sintassi da \[ [rappresentare \_ come](/windows/desktop/Midl/represent-as) \] . Come per l'attributo IDL, \[ [wire \_ marshal,](/windows/desktop/Midl/wire-marshal)offre un modo più efficiente per effettuare il \] marshalling dei dati in una rete. Come attributo ACF, il **\[ \_ marshalling utente \]** consente di effettuare il marshalling di tipi di dati personalizzati sconosciuti a MIDL. Ogni tipo specifico dell'applicazione ha un tipo trasmettibile corrispondente che definisce la rappresentazione in transito.

Il tipo specifico dell'applicazione può essere un tipo semplice, composito o puntatore. La restrizione principale è che l'istanza del tipo deve avere una dimensione di memoria fissa e ben definita. Se le dimensioni dell'istanza del tipo devono cambiare, usare un campo puntatore anziché una matrice conforme. In alternativa, è possibile definire un puntatore al tipo modificabile.

Come per **\[ l'attributo wire \_ marshal, \]** si forniscono routine per i passaggi di ridimensionamento, marshalling, annullamento del marshalling e liberamento. Nella tabella seguente vengono descritti i quattro nomi di routine forniti dall'utente. è <type> il tipo userm-*specificato nella* definizione del tipo **\[ di \_ marshalling \]** dell'utente.



| Routine                                                            | Descrizione                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_UserSize](the-type-usersize-function.md)           | Ridimensiona il buffer di dati RPC prima del marshalling sul lato client o server. |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | Effettua il marshalling dei dati sul lato client o server.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Annulla ilmarshaling dei dati sul lato client o server.                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | Libera i dati sul lato server.                                        |



 

Queste routine fornite dall'utente vengono fornite dal client o dall'applicazione server, in base agli attributi direzionali.

Se il parametro è \[ [solo in](/windows/desktop/Midl/in) \] , il client trasmette al server. Il client necessita **<type> \_ delle funzioni UserSize** **<type> \_ e UserMarshal.** Il server richiede le **<type> \_ funzioni UserUnmarshal** **<type> \_ e UserFree.**

Per un \[ [parametro](/windows/desktop/Midl/out-idl) \] out-only, il server trasmette al client. Il server necessita **<type> \_ delle funzioni UserSize** **<type> \_ e UserMarshal,** mentre il client necessita **<type> \_ della funzione UserMarshal.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributo wire \_ marshal](the-wire-marshal-attribute.md)
</dt> <dt>

[Regole di marshalling per il marshalling dell'utente e il wire \_ marshal](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[marshalling \_ utente](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 