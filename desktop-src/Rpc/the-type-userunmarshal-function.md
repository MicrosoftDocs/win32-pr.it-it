---
title: Funzione type_UserUnmarshal
description: Il tipo \_ UserUnmarshal Function è una funzione di supporto per gli attributi \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047319"
---
# <a name="the-type_userunmarshal-function"></a>Funzione di tipo \_ UserUnmarshal

La funzione **<type> \_ UserUnmarshal** è una funzione di supporto per il \[ [ \_ marshalling di rete](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi del [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] . Gli stub chiamano questa funzione per eseguire l'unmarshalling dei dati sul lato client o server. La funzione è definita come segue:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<type>Nel nome della funzione indica il tipo di utente specificato nella definizione del **\[ \_ marshalling \] di rete** o del tipo di **\[ \_ \] marshalling dell'utente** . Questo tipo può essere untransmittable o even, se usato con l'attributo **\[ \_ Marshal \] dell'utente** , sconosciuto al compilatore MIDL. Il nome del tipo Wire (il nome del tipo trasmissibile) non viene usato nel prototipo di funzione. Si noti, tuttavia, che il tipo Wire definisce il layout Wire per i dati come specificato da OSF DCE.

Il parametro *pFlags* è un puntatore a un campo **unsigned long** flag. La parola superiore del flag contiene i flag di rappresentazione dei dati NDR come definito da OSF DCE per la virgola mobile, l'ordine dei byte e le rappresentazioni di caratteri. La parola inferiore contiene un flag di contesto di marshalling definito dal canale COM. Il layout esatto dei flag all'interno del campo viene descritto nella [funzione di tipo \_ UserSize](the-type-usersize-function.md).

Il parametro *pbuffer* è il puntatore del buffer corrente. Il puntatore potrebbe non essere allineato alla voce. La funzione **<type> \_ UserUnmarshal** deve allineare il puntatore del buffer in modo appropriato, annullare il marshalling dei dati e restituire la nuova posizione del buffer, ovvero l'indirizzo del primo byte dopo l'oggetto di cui è stato eseguito l'unmarshalling.

Il parametro *pMyObj* è un puntatore a un oggetto di tipo definito dall'utente.

In un ambiente eterogeneo, il motore NDR esegue qualsiasi conversione dei dati necessaria prima di chiamare la funzione **<type> \_ UserUnmarshal** . Si noti che il motore di NDR esegue questa conversione dei dati in base alla definizione di tipo Wire specificata per questo tipo di dati utente. Il flag indica la rappresentazione dati del mittente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Regole di marshalling per \_ marshalling utente e \_ marshalling di rete](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshalling di rete](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_marshalling utente](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 