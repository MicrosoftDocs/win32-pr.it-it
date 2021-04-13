---
title: Funzione type_UserMarshal
description: Il tipo \_ UserMarshal Function è una funzione di supporto per gli attributi \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399685"
---
# <a name="the-type_usermarshal-function"></a>Funzione di tipo \_ UserMarshal

La funzione **<type> \_ UserMarshal** è una funzione di supporto per il \[ [ \_ marshalling di rete](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi del [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] . Gli stub chiamano questa funzione per effettuare il marshalling dei dati sul lato client o server. La funzione è definita come segue:

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<type>Nel nome della funzione indica il tipo di utente specificato nella definizione del **\[ \_ marshalling \] di rete** o del tipo di **\[ \_ \] marshalling dell'utente** . Questo tipo può essere untransmittable o even, se usato con l'attributo **\[ \_ Marshal \] utente** , un tipo sconosciuto al compilatore MIDL. Il nome del tipo Wire (il nome del tipo trasmissibile) non viene usato nel prototipo di funzione. Si noti, tuttavia, che il tipo Wire definisce il layout Wire per i dati come specificato da OSF DCE.

Il parametro *pFlags* è un puntatore a un campo unsigned long flag. La parola superiore del flag contiene i flag di rappresentazione dei dati NDR come definito da OSF DCE per la virgola mobile, l'ordine dei byte e le rappresentazioni di caratteri. La parola inferiore contiene un flag di contesto di marshalling definito dal canale COM. Il layout esatto dei flag all'interno del campo viene descritto nella [funzione di tipo \_ UserSize](the-type-usersize-function.md).

Il parametro *pbuffer* è il puntatore del buffer corrente. Il puntatore potrebbe non essere allineato alla voce. La funzione **<type> \_ UserMarshal** deve allineare il puntatore del buffer in modo appropriato, effettuare il marshalling dei dati e restituire la nuova posizione del buffer, ovvero l'indirizzo del primo byte dopo l'oggetto di cui è stato effettuato il marshalling. Tenere presente che la specifica del tipo Wire determina il layout effettivo dei dati nel buffer.

Il parametro *pMyObj* è un puntatore a un oggetto tipo utente.

Il valore restituito è la nuova posizione del buffer, ovvero l'indirizzo del primo byte dopo l'oggetto di cui è stato eseguito l'unmarshalling.

L'overflow del buffer può verificarsi quando si calcolano erroneamente le dimensioni dei dati e si tenta di effettuare il marshalling di più dati del previsto. È necessario prestare attenzione per evitare questa situazione. Per verificarlo, è possibile usare il puntatore restituito da **<type> \_ UserMarshal** . In caso contrario, si rischia che il motore di NDR generi un'eccezione di overflow del buffer in un secondo momento.

Le eccezioni devono essere rilevate e gestite localmente, le eccezioni non devono essere consentite per propigated lo stack di chiamate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Regole di marshalling per \_ marshalling utente e \_ marshalling di rete](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshalling di rete](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_marshalling utente](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 