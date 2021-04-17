---
title: Attributo user_marshal
description: L'attributo \ User \_ Marshal \ è un attributo di tipo ACF simile alla sintassi di \ rappresenta \_ come \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- RPC, attributi, user_marshal di procedura remota
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473806"
---
# <a name="the-user_marshal-attribute"></a>\_Attributo Marshal utente

L' \[ [attributo \_ Marshal utente](/windows/desktop/Midl/user-marshal) \] è un attributo di tipo ACF simile a sintassi per \[ [rappresentare \_ come](/windows/desktop/Midl/represent-as) \] . Come per l'attributo IDL, \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] , offre un modo più efficiente per effettuare il marshalling dei dati in una rete. Come attributo ACF, il **\[ \_ marshalling \] degli utenti** consente di effettuare il marshalling dei tipi di dati personalizzati sconosciuti a MIDL. Ogni tipo specifico dell'applicazione ha un tipo transmittable corrispondente che definisce la rappresentazione in transito.

Il tipo specifico dell'applicazione può essere un tipo semplice, composto o puntatore. La restrizione principale è che l'istanza del tipo deve avere una dimensione di memoria fissa e ben definita. Se è necessario modificare le dimensioni dell'istanza del tipo, utilizzare un campo puntatore anziché una matrice conforme. In alternativa, è possibile definire un puntatore al tipo modificabile.

Come per l'attributo **\[ Wire \_ Marshal \]** , vengono fornite routine per il ridimensionamento, il marshalling, l'unmarshalling e il rilascio di passaggi. Nella tabella seguente vengono descritti i quattro nomi di routine specificati dall'utente. <type>È il *tipo* di utente specificato nella definizione del tipo di **\[ \_ marshalling \] dell'utente** .



| Routine                                                            | Descrizione                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_UserSize](the-type-usersize-function.md)           | Ridimensiona il buffer di dati RPC prima del marshalling sul lato client o server. |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | Esegue il marshalling dei dati sul lato client o server.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Esegue l'unmarshalling dei dati sul lato client o server.                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | Libera i dati sul lato server.                                        |



 

Queste routine fornite dall'utente vengono fornite dal client o dall'applicazione server, in base agli attributi direzionali.

Se il parametro è \[ solo [in](/windows/desktop/Midl/in) \] , il client trasmette al server. Il client richiede le funzioni **<type> \_ UserSize** e **<type> \_ UserMarshal** . Per il server sono necessarie le funzioni **<type> \_ UserUnmarshal** e **<type> \_ UserFree** .

Per un \[ [](/windows/desktop/Midl/out-idl) \] parametro di sola uscita, il server trasmette al client. Il server necessita delle funzioni **<type> \_ UserSize** e **<type> \_ UserMarshal** , mentre il client richiede la funzione **<type> \_ UserMarshal** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributo Wire \_ Marshal](the-wire-marshal-attribute.md)
</dt> <dt>

[Regole di marshalling per marshalling utente e \_ marshalling di rete](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshalling utente](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[\_marshalling di rete](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 