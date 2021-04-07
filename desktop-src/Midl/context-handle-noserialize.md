---
title: attributo context_handle_noserialize
description: L'attributo \ Context \_ handle \_ noserialize \ ACF garantisce che un handle di contesto non verrà mai serializzato, indipendentemente dal comportamento predefinito dell'applicazione.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- attributo context_handle_noserialize MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724962"
---
# <a name="context_handle_noserialize-attribute"></a>\_attributo noserialize dell'handle di contesto \_

L'attributo dell' **\[ handle di contesto \_ \_ noserialize \]** ACF garantisce che un handle di contesto non venga mai serializzato, indipendentemente dal comportamento predefinito dell'applicazione.

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo-ACF-Attribute-List* 
</dt> <dd>

Qualsiasi altro attributo ACF applicabile al tipo.

</dd> <dt>

*context-handle-tipo* 
</dt> <dd>

Identificatore che specifica il tipo di handle del contesto, come definito in una Dichiarazione [**typedef**](typedef.md) . Si tratta del tipo che riceve l'attributo dell' [**\[ \_ handle \] del contesto**](context-handle.md) nel file IDL.

</dd> <dt>

*funzione-ACF-Attribute-List* 
</dt> <dd>

Eventuali attributi ACF aggiuntivi che si applicano alla funzione.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Nome della funzione come definito nel file IDL.

</dd> <dt>

*parametro-ACF-Attribute-List* 
</dt> <dd>

Qualsiasi altro attributo ACF applicabile al parametro.

</dd> <dt>

*nome param* 
</dt> <dd>

Nome del parametro come definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo dell' [**\[ \_ handle \] di contesto**](context-handle.md) identifica un handle di associazione che mantiene le informazioni sul contesto o sullo stato sul server tra le chiamate a procedure remote. L'attributo può essere visualizzato come un attributo di tipo [**typedef**](typedef.md) IDL, come attributo di tipo restituito della funzione o come attributo di parametro.

Per impostazione predefinita, le chiamate agli handle di contesto vengono serializzate. Un'applicazione può chiamare [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) per eseguire l'override di questo comportamento predefinito. L'utilizzo dell'attributo [**\[ \_ handle \] di contesto**](context-handle.md) in un file ACF garantisce che le chiamate su questo particolare handle di contesto non verranno serializzate, indipendentemente dal comportamento dell'applicazione chiamante. La fornitura di una routine di rundown del contesto è facoltativa.

Questo attributo è disponibile nella versione MIDL 5,0.

**Windows server 2003 e Windows XP o versione successiva:** Una singola interfaccia può supportare sia gli handle di contesto serializzati che quelli non serializzati, consentendo a un metodo su un'interfaccia di accedere a un handle di contesto esclusivamente (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzato). Queste funzionalità di accesso sono confrontabili con i meccanismi di blocco in lettura/scrittura; i metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori). I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati. I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che leggono semplicemente da un handle di contesto, possono essere non serializzati. Si noti che i metodi di creazione vengono serializzati in modo implicito.

## <a name="examples"></a>Esempi

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Attributi ACF](acf-attributes.md)
</dt> <dt>

[**\_serializzazione handle di contesto \_**](context-handle-serialize.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[Handle di contesto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[Routine di esecuzione del contesto del server](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[Client multithreading e handle di contesto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 