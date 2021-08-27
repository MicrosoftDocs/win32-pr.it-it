---
title: Attributo user_marshal
description: L'attributo \ user marshal\ è un attributo di tipo ACF simile \_ nella sintassi a \ represent \_ as\ .
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Chiamata di procedura remota RPC, attributi, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b769e6a7e176d5aeba68afd322cdd6f24d76c6b5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883750"
---
# <a name="the-user_marshal-attribute"></a>Attributo di \_ marshalling dell'utente

\[ [L'attributo di \_ marshalling](/windows/desktop/Midl/user-marshal) \] utente è un attributo di tipo ACF simile nella sintassi da \[ [rappresentare \_ come](/windows/desktop/Midl/represent-as) \] . Come per l'attributo IDL, wire marshal, offre un modo più efficiente per effettuare il \[ [ \_ ](/windows/desktop/Midl/wire-marshal) \] marshalling dei dati in una rete. Come attributo ACF, **\[ il \_ marshalling utente \]** consente di effettuare il marshalling di tipi di dati personalizzati sconosciuti a MIDL. Ogni tipo specifico dell'applicazione ha un tipo trasmettibile corrispondente che definisce la rappresentazione del cavo.

Il tipo specifico dell'applicazione può essere un tipo semplice, composito o puntatore. La restrizione principale è che l'istanza del tipo deve avere una dimensione di memoria fissa e ben definita. Se le dimensioni dell'istanza del tipo devono cambiare, usare un campo puntatore anziché una matrice conforme. In alternativa, è possibile definire un puntatore al tipo modificabile.

Come per **\[ l'attributo wire \_ marshal, \]** si forniscono routine per i passaggi di ridimensionamento, marshalling, annullamento del marshalling e liberamento. Nella tabella seguente vengono descritti i quattro nomi di routine forniti dall'utente. Il &lt; tipo è il tipo &gt; userm-*specificato* nella definizione del tipo **\[ di \_ marshalling \]** utente.



| Routine                                                            | Descrizione                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [&lt;digitare &gt; \_ UserSize](the-type-usersize-function.md)           | Ridimensiona il buffer di dati RPC prima del marshalling sul lato client o server. |
| [&lt;digitare &gt; \_ UserMarshal](the-type-usermarshal-function.md)     | Esegue il marshalling dei dati sul lato client o server.                           |
| [&lt;digitare &gt; \_ UserUnmarshal](the-type-userunmarshal-function.md) | Annulla ilmarshaling dei dati sul lato client o server.                         |
| [&lt;digitare &gt; \_ UserFree](the-type-userfree-function.md)           | Libera i dati sul lato server.                                        |



 

Queste routine fornite dall'utente vengono fornite dal client o dall'applicazione server, in base agli attributi direzionali.

Se il parametro è \[ [solo in](/windows/desktop/Midl/in) \] , il client trasmette al server. Il client richiede il **&lt; tipo &gt; \_ UserSize** e **&lt; le funzioni &gt; \_ UserMarshal.** Il server richiede il **&lt; tipo &gt; \_ UserUnmarshal** e **&lt; le funzioni &gt; \_ UserFree.**

Per un \[ [parametro out](/windows/desktop/Midl/out-idl) \] -only, il server trasmette al client. Il server richiede il **&lt; tipo &gt; \_ UserSize** e **&lt; le funzioni &gt; \_ UserMarshal,** mentre il client richiede la **&lt; funzione &gt; \_ UserMarshal.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributo wire \_ marshal](the-wire-marshal-attribute.md)
</dt> <dt>

[Regole di marshalling per il marshalling utente e il \_ marshalling del wire](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[marshalling \_ utente](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 
