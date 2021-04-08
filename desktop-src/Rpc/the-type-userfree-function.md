---
title: Funzione type_UserFree
description: Il tipo \_ UserFree Function è una funzione di supporto per gli attributi \ Wire \_ Marshal \ e \ User \_ Marshal \.
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727442"
---
# <a name="the-type_userfree-function"></a>Funzione di tipo \_ UserFree

La funzione **<type> \_ UserFree** è una funzione di supporto per il \[ [ \_ marshalling di rete](/windows/desktop/Midl/wire-marshal) \] e \[ gli attributi del [ \_ marshalling degli utenti](/windows/desktop/Midl/user-marshal) \] . Gli stub chiamano questa funzione per liberare i dati sul lato server. La funzione è definita come segue:

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<type>Nel nome della funzione indica il tipo di utente specificato nella definizione del **\[ \_ marshalling \] di rete** o del tipo di **\[ \_ \] marshalling dell'utente** .

Il parametro *pFlags* è un puntatore a un campo **unsigned long** flag. La parola superiore del flag contiene i flag di rappresentazione dei dati NDR come definito da OSF DCE per la virgola mobile, l'ordine dei byte e le rappresentazioni di caratteri. La parola inferiore contiene un flag di contesto di marshalling definito dal canale COM. Il layout esatto dei flag all'interno del campo viene descritto nella [funzione di tipo \_ UserSize](the-type-usersize-function.md).

Il parametro *pMyObj* è un puntatore a un oggetto tipo utente. Il motore NDR libera l'oggetto di primo livello. L'utente è responsabile di liberare tutti gli oggetti a cui può puntare l'oggetto di primo livello.

Le eccezioni devono essere rilevate e gestite localmente, le eccezioni non devono essere consentite per propigated lo stack di chiamate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Regole di marshalling per \_ marshalling utente e \_ marshalling di rete](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_marshalling di rete](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[\_marshalling utente](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 