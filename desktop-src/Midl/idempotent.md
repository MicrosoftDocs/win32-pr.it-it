---
title: Attributo idempotente
description: L'attributo \ idempotent\ specifica che un'operazione non modifica le informazioni sullo stato e restituisce gli stessi risultati ogni volta che viene eseguita. L'esecuzione della routine più volte ha lo stesso effetto dell'esecuzione di una sola volta.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- Attributo idempotente MIDL
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a4135fdcb38fbad9e41b04a136f69420da7455f68d38a0c507135892e2a00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895221"
---
# <a name="idempotent-attribute"></a>Attributo idempotente

**\[ L'attributo idempotente \]** specifica che un'operazione non modifica le informazioni sullo stato e restituisce gli stessi risultati ogni volta che viene eseguita. L'esecuzione della routine più volte ha lo stesso effetto dell'esecuzione di una sola volta.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Specifica un elenco di zero o più attributi IDL che si applicano all'intera interfaccia. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Specifica attributi aggiuntivi da applicare alla funzione. Separare più attributi con virgole.

</dd> <dt>

*Returntype* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione a cui verrà applicato l'attributo **\[ \] idempotente.**

</dd> <dt>

*params* 
</dt> <dd>

Elenco di parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

RPC supporta due tipi di semantica delle chiamate remote: chiamate a operazioni con l'attributo **\[ idempotente \]** e chiamate a operazioni *(operazioni idempotenti)* senza l'attributo **\[ idempotente \]** (operazioni *non idempotenti).* Un'operazione idempotente può essere eseguita più di una volta senza alcun effetto negativo. Al contrario, un'operazione non idempotente non può essere eseguita più di una volta perché restituirà risultati diversi ogni volta o perché modifica uno stato.

Per assicurarsi che una procedura viene eseguita di nuovo automaticamente se la chiamata non viene completata, usare **\[ l'attributo \] idempotente.** Se gli **\[ attributi \] idempotenti**, broadcast o forse non sono presenti, la procedura userà la **\[** [](broadcast.md) **\]** **\[** [](maybe.md) **\]** semantica non idempotente per impostazione predefinita. In questo caso, l'operazione viene eseguita una sola volta.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trasmissione**](broadcast.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Forse**](maybe.md)
</dt> </dl>

 

 




