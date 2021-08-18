---
title: context_handle_serialize attributo
description: L'attributo \ context handle serialize\ ACF garantisce che un handle di contesto verrà sempre serializzato, indipendentemente dal comportamento predefinito \_ \_ dell'applicazione.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize attributo MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91bf9ab1610585001b1380b15ba5a89433f80194596e26cbae84692ff3a872a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013959"
---
# <a name="context_handle_serialize-attribute"></a>Attributo di \_ \_ serializzazione dell'handle di contesto

L'attributo ACF **\[ \_ \_ di serializzazione \]** dell'handle di contesto garantisce che un handle di contesto sia sempre serializzato, indipendentemente dal comportamento predefinito dell'applicazione.

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*type-acf-attribute-list* 
</dt> <dd>

Qualsiasi altro attributo ACF che si applica al tipo.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Identificatore che specifica il tipo di handle di contesto, come definito in una [**dichiarazione typedef.**](typedef.md) Si tratta del tipo che riceve **\[ l'attributo di \_ \_ serializzazione \] dell'handle** di contesto nel file IDL.

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

Nome del parametro come definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo di \_ \_ serializzazione dell'handle \]** di contesto identifica un handle di associazione che gestisce informazioni sul contesto o sullo stato nel server tra chiamate di procedura remota. L'attributo può essere visualizzato come attributo di [**tipo typedef**](typedef.md) IDL, come attributo del tipo restituito della funzione o come attributo di parametro.

Per impostazione predefinita, le chiamate sugli handle di contesto vengono serializzate, ma un'applicazione può chiamare [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) per eseguire l'override di questo comportamento predefinito. L'uso dell'attributo **\[ \_ di \_ serializzazione \] dell'handle** di contesto in un file ACF garantisce che le chiamate a questo handle di contesto specifico vengano serializzate, anche se l'applicazione chiamante ha eseguito l'override della serializzazione predefinita. Una routine di rundown del contesto è facoltativa.

Questo attributo è disponibile in MIDL versione 5.0.

**Windows Server 2003 e Windows XP o versioni successive:** Una singola interfaccia può contenere handle di contesto serializzati e non serializzati, consentendo a un metodo in un'interfaccia di accedere esclusivamente a un handle di contesto (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzata). Queste funzionalità di accesso sono paragonabili ai meccanismi di blocco in lettura/scrittura. I metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori). I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati. I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che leggono semplicemente da un handle di contesto, possono essere nonserializzati. Si noti che i metodi di creazione vengono serializzati in modo implicito.

## <a name="examples"></a>Esempi

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Attributi ACF](acf-attributes.md)
</dt> <dt>

[**context \_ handle \_ noserialize**](context-handle-noserialize.md)
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

 

 