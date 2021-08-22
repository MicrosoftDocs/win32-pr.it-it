---
title: context_handle_noserialize attributo
description: L'attributo \ context \_ handle noserialize\ ACF garantisce che un handle di contesto non verrà mai serializzato, indipendentemente dal comportamento \_ predefinito dell'applicazione.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize attributo MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40556db0d63441e42d46a0ed7f9bd45edb8b2ce65f8d4b9b84e3a848325ddbb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013999"
---
# <a name="context_handle_noserialize-attribute"></a>attributo \_ context handle \_ noserialize

**\[ \_ L'attributo \_ ACF \] noserialize** dell'handle di contesto garantisce che un handle di contesto non verrà mai serializzato, indipendentemente dal comportamento predefinito dell'applicazione.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*type-acf-attribute-list* 
</dt> <dd>

Qualsiasi altro attributo ACF che si applica al tipo.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Identificatore che specifica il tipo di handle di contesto, come definito in una [**dichiarazione typedef.**](typedef.md) Si tratta del tipo che riceve [**\[ l'attributo di \_ handle \]**](context-handle.md) di contesto nel file IDL.

</dd> <dt>

*function-acf-attribute-list* 
</dt> <dd>

Eventuali attributi ACF aggiuntivi che si applicano alla funzione.

</dd> <dt>

*function-name* 
</dt> <dd>

Nome della funzione come definito nel file IDL.

</dd> <dt>

*parameter-acf-attribute-list* 
</dt> <dd>

Qualsiasi altro attributo ACF che si applica al parametro .

</dd> <dt>

*param-name* 
</dt> <dd>

Nome del parametro definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

[**\[ L'attributo \_ dell'handle \]**](context-handle.md) di contesto identifica un handle di associazione che mantiene le informazioni sul contesto o sullo stato nel server tra chiamate di procedura remota. L'attributo può essere visualizzato come attributo di tipo [**typedef**](typedef.md) IDL, come attributo di tipo restituito di funzione o come attributo di parametro.

Per impostazione predefinita, le chiamate sugli handle di contesto vengono serializzate. Un'applicazione può chiamare [**RpcSsDontSerializeContext per**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) eseguire l'override di questo comportamento predefinito. [**\[ L'uso dell'attributo \_ \]**](context-handle.md) di handle di contesto in un file ACF garantisce che le chiamate a questo handle di contesto specifico non verranno serializzate, indipendentemente dal comportamento dell'applicazione chiamante. Fornire una routine di rundown del contesto è facoltativa.

Questo attributo è disponibile in MIDL versione 5.0.

**Windows ServerÂ 2003 e Windows XP o versioni successive:** Una singola interfaccia può contenere handle di contesto serializzati e non serializzati, consentendo a un metodo di un'interfaccia di accedere esclusivamente a un handle di contesto (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzata). Queste funzionalità di accesso sono paragonabili ai meccanismi di blocco in lettura/scrittura. I metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori). I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati. I metodi che non modificano lo stato di un handle di contesto, ad esempio quelli che leggono semplicemente da un handle di contesto, possono essere nonserializzati. Si noti che i metodi di creazione vengono serializzati in modo implicito.

## <a name="examples"></a>Esempi

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Attributi ACF](acf-attributes.md)
</dt> <dt>

[**serializzazione \_ dell'handle \_ di contesto**](context-handle-serialize.md)
</dt> <dt>

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[Handle di contesto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Routine di esecuzione del contesto del server](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Client multithreading e handle di contesto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 