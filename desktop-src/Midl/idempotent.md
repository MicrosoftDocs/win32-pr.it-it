---
title: attributo idempotente
description: L'attributo \ idempotente \ specifica che un'operazione non modifica le informazioni sullo stato e restituisce gli stessi risultati ogni volta che viene eseguita. L'esecuzione della routine più di una volta ha lo stesso effetto dell'esecuzione di una sola volta.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- attributo MIDL di idempotente
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516219"
---
# <a name="idempotent-attribute"></a>attributo idempotente

L'attributo **\[ idempotente \]** specifica che un'operazione non modifica le informazioni di stato e restituisce gli stessi risultati ogni volta che viene eseguita. L'esecuzione della routine più di una volta ha lo stesso effetto dell'esecuzione di una sola volta.

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

*Interface-Attribute-List* 
</dt> <dd>

Specifica un elenco di zero o più attributi IDL che si applicano all'interfaccia nel suo complesso. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*elenco attributi* 
</dt> <dd>

Specifica gli attributi aggiuntivi da applicare alla funzione. Separare più attributi con virgole.

</dd> <dt>

*returnType* 
</dt> <dd>

Specifica il tipo restituito della funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione a cui verrà applicato l'attributo **\[ idempotente \]** .

</dd> <dt>

*params* 
</dt> <dd>

Elenco dei parametri della funzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

RPC supporta due tipi di semantica di chiamata remota: le chiamate alle operazioni con l'attributo **\[ idempotente \]** e le chiamate alle operazioni (operazioni *idempotente* ) senza l'attributo **\[ idempotente \]** (operazioni *non idempotente* ). Un'operazione idempotente può essere eseguita più di una volta senza effetti negativi. Viceversa, un'operazione non idempotente non può essere eseguita più di una volta perché restituirà risultati diversi ogni volta o perché modifica uno stato.

Per assicurarsi che una routine venga eseguita di nuovo automaticamente se la chiamata non viene completata, utilizzare l'attributo **\[ idempotente \]** . Se gli attributi **\[ \] idempotente**, **\[** [**broadcast**](broadcast.md) **\]** o **\[** [**Maybe**](maybe.md) **\]** non sono presenti, per impostazione predefinita la procedura utilizzerà la semantica non idempotente. In questo caso, l'operazione viene eseguita una sola volta.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**trasmissione**](broadcast.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Forse**](maybe.md)
</dt> </dl>

 

 




