---
title: Message (attributo)
description: L'attributo \ Message \ indica che la chiamata di procedura remota deve essere considerata come un messaggio dal client al server.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- MIDL attributo messaggio
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472939"
---
# <a name="message-attribute"></a>Message (attributo)

L'attributo **\[ message \]** indica che la chiamata di procedura remota deve essere considerata come un messaggio dal client al server.

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Altri attributi che si applicano alla funzione. **\[** [](local.md) **\]** **\[** [](nocode.md) **\]** **\[** [](code.md)**\]** **\[** [](optimize.md) **\]** Con l'attributo **\[ message \]** è possibile utilizzare solo gli attributi local, NoCode, code e optimize.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Nome della funzione come definito nel file IDL.

</dd> <dt>

*facoltativo-parameter-attributes* 
</dt> <dd>

Zero o più attributi MIDL che verranno applicati al parametro.

</dd> <dt>

*nome param* 
</dt> <dd>

Nome del parametro come definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Come messaggi dal client, le chiamate a procedure remote con l'attributo **\[ message \]** vengono recapitate al server in modo asincrono tramite il trasporto di Accodamento messaggi di [**ncadg \_ mq**](ncadg-mq.md) . È possibile indicare la messaggistica in modalità sincrona specificando il protocollo di trasporto **ncadg \_ mq** senza usare l'attributo **\[ \] Message** .

Specificando la messaggistica in modalità asincrona, l'attributo **\[ message \]** consente al client di eseguire la chiamata di procedura remota e restituire immediatamente un risultato, anche quando l'applicazione server non risponde. Se il server di destinazione non è disponibile, la chiamata verrà archiviata fino a quando il server non sarà disponibile.

La messaggistica in modalità asincrona consente inoltre di controllare le proprietà della coda di messaggi della coda di ricezione per il server. Per ulteriori informazioni su come selezionare la qualità del servizio, la priorità delle chiamate e la durata delle chiamate per il processo server, vedere [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) .

All'attributo del **\[ messaggio \]** si applicano anche le restrizioni seguenti:

-   Microsoft Message Queuing deve essere implementato nei sistemi client e server e i sistemi devono essere visibili tra loro in base a quanto determinato dall'ambito dell'installazione della coda di messaggi.
-   L'associazione deve usare endpoint noti e il protocollo di trasporto [**ncadg \_ mq**](ncadg-mq.md) .
-   La funzione non può contenere parametri di output o un tipo restituito diverso da [**void**](void.md). Si noti che la seconda restrizione rende attualmente l'attributo del **\[ messaggio \]** non adatto per i metodi di interfaccia com (Object). La versione successiva di MIDL consentirà alle funzioni di **\[ \] messaggio** di restituire \_ lo stato di errore \_ t o HRESULT.
-   Qualsiasi interfaccia che contiene almeno una chiamata al **\[ \] messaggio** deve essere registrata chiamando [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) o [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) prima di chiamare [**RpcServerUseProtseqEpEx (ncadg \_ mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex). In caso contrario, le chiamate in attesa nella coda per il server verranno lette prima che l'interfaccia venga registrata e le chiamate avranno esito negativo.

## <a name="examples"></a>Esempi

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**codice**](code.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**ncadg \_ mq**](ncadg-mq.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**ottimizzare**](optimize.md)
</dt> <dt>

[Accodamento messaggi RPC](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 