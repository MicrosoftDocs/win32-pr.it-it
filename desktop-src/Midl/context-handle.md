---
title: attributo context_handle
description: L'attributo \ Context \_ handle \ identifica un handle di associazione che mantiene le informazioni sul contesto o sullo stato sul server tra le chiamate a procedure remote.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- attributo context_handle MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724959"
---
# <a name="context_handle-attribute"></a>\_attributo handle di contesto

L'attributo dell' **\[ \_ handle \] di contesto** identifica un handle di associazione che mantiene le informazioni sul contesto o sullo stato sul server tra le chiamate a procedure remote.

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un tipo di puntatore o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*dichiaratore e declarator-list* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Il dichiaratore per un handle di contesto deve includere almeno un dichiaratore di puntatore. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il *declarator-list* è costituito da uno o più dichiaratori, separati da virgole. L'identificatore di nome parametro nel dichiaratore di funzione è facoltativo.

</dd> <dt>

*Function-attr-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[ Context \_ handle \]**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' **\*** indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi direzionali, attributi di campo, attributi di utilizzo e attributi del puntatore appropriati per il tipo di parametro specificato. Separare più attributi con virgole.

</dd> <dt>

*context-handle-tipo* 
</dt> <dd>

Specifica l'identificatore che specifica il tipo di handle di contesto come definito in una Dichiarazione [**typedef**](typedef.md) che accetta l'attributo dell' **\[ \_ handle \] di contesto** . La routine di rundown è facoltativa.

**Windows server 2003 e Windows XP:** Una singola interfaccia può supportare sia gli handle di contesto serializzati che quelli non serializzati, consentendo a un metodo su un'interfaccia di accedere a un handle di contesto esclusivamente (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzato). Queste funzionalità di accesso sono confrontabili con i meccanismi di blocco in lettura/scrittura; i metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori). I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati. I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che leggono semplicemente da un handle di contesto, possono essere non serializzati. Si noti che i metodi di creazione vengono serializzati in modo implicito.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo dell' **\[ \_ handle \] di contesto** può essere visualizzato come un attributo di tipo [**typedef**](typedef.md) IDL, come attributo di tipo restituito della funzione o come attributo di parametro. Quando si applica l'attributo dell' **\[ \_ handle \] di contesto** a una definizione di tipo, è necessario fornire anche una routine di rundown del contesto. Per informazioni dettagliate, vedere [routine di esecuzione del contesto server](/windows/desktop/Rpc/server-context-run-down-routine) .

Quando si usa il compilatore MIDL in modalità predefinita ([**/MS \_ ext**](-ms-ext.md)), un handle di contesto può essere qualsiasi tipo di puntatore selezionato dall'utente, purché sia conforme ai requisiti per gli handle di contesto descritti qui. I dati associati a tale tipo di handle del contesto non vengono trasmessi sulla rete e devono essere modificati solo dall'applicazione server. I compilatori IDL DCE limitano gli handle di contesto ai puntatori di tipo [**void**](void.md) **\*** . Questa funzionalità non è pertanto disponibile quando si usa l'opzione [**/OSF**](-osf.md) del compilatore MIDL.

Come per gli altri tipi di handle, l'handle di contesto è opaco per l'applicazione client e qualsiasi dato associato non viene trasmesso. Sul server, l'handle di contesto funge da handle sul contesto attivo e tutti i dati associati al tipo di handle di contesto sono accessibili.

Per creare un handle di contesto, il client passa al server un **\[** [](out-idl.md) **\]** puntatore out, **\[** [**ref**](ref.md) **\]** a un handle di contesto. Il punto di controllo del contesto può avere un valore **null** o non **null** , purché il relativo valore sia coerente con i relativi attributi del puntatore. Ad esempio, quando al tipo di handle del contesto è **\[** [](ref.md) **\]** applicato l'attributo ref, non può avere un valore **null** . È necessario fornire un altro handle di binding per completare l'associazione fino a quando non viene creato l'handle del contesto. Quando non viene specificato alcun handle esplicito, viene usata l'associazione implicita. Quando non **\[** è presente alcun attributo [**\_ handle implicito**](implicit-handle.md) **\]** , viene usato un handle automatico.

La procedura remota nel server crea un handle di contesto attivo. Il client deve usare tale handle di contesto come **\[** [**un**](in.md) **\]** parametro **\[** **out \]** in o in chiamate successive. Un handle **\[ \] di** contesto unico può essere usato come handle di associazione, quindi deve avere un valore non **null** . Un handle **\[ di contesto in \]** sola non riflette le modifiche di stato nel server.

Nel server, la procedura chiamata può interpretare l'handle del contesto in base alle esigenze. La stored procedure chiamata, ad esempio, può allocare l'archiviazione heap e utilizzare l'handle di contesto come puntatore a questa risorsa di archiviazione.

Per chiudere un handle di contesto, il client passa l'handle del contesto come un **\[** argomento [**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** . Il server deve restituire un handle di contesto **null** quando non è più in grado di mantenere il contesto per conto del chiamante. Se, ad esempio, l'handle di contesto rappresenta un file aperto e la chiamata chiude il file, il server deve impostare l'handle di contesto su **null** e restituirlo al client. Un valore **null** non è valido come handle di associazione nelle chiamate successive.

Un handle di contesto è valido solo per un server. Quando una funzione dispone di due parametri di handle e l'handle del contesto non è **null**, gli handle di associazione devono fare riferimento allo stesso spazio di indirizzi.

Quando una funzione dispone di un oggetto **\[** [**in**](in.md) **\]** o un oggetto **\[ in**, **\]** il relativo handle di contesto può essere utilizzato come handle di associazione. In questo caso, l'associazione implicita non viene utilizzata e l' **\[** [**\_ handle implicito**](implicit-handle.md) **\]** o l' **\[** attributo [**\_ handle automatico**](auto-handle.md) **\]** viene ignorato.

Per gli handle di contesto si applicano le restrizioni seguenti:

-   Gli handle del contesto non possono essere elementi della matrice, membri della struttura o membri di Unione. Possono essere solo parametri.
-   Gli handle del contesto non possono avere la **\[** [**trasmissione \_ As**](transmit-as.md) **\]** o **\[** [**rappresentare \_ come**](represent-as.md) **\]** attributo.
-   I parametri che sono puntatori a **\[** [](out-idl.md) **\]** handle di contesto out devono essere **\[** [](ref.md) **\]** puntatori Ref.
-   Un **\[** [](in.md) **\]** handle nel contesto può essere utilizzato come handle di associazione e non può essere **null**.
-   Un handle di contesto [**out**](out-idl.md) può essere **null** nell'input, ma solo se la stored procedure ha un altro parametro **\[ di** handle esplicito. Se non sono presenti altri parametri **\[ di handle di** contesto non **null** espliciti, l'handle di contesto in, **out \]** non può essere **null**.
-   Non è possibile usare un handle di contesto con i callback.

## <a name="examples"></a>Esempi

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[**\_handle automatico**](auto-handle.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[Ripristino del contesto client](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Handle di contesto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**gestire**](handle.md)
</dt> <dt>

[Binding e handle](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**handle implicito \_**](implicit-handle.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[Client multithreading e handle di contesto](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**rappresenta \_ come**](represent-as.md)
</dt> <dt>

[**RpcSsDestroyClientContext**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[Routine di esecuzione del contesto del server](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Trasmetti \_ come**](transmit-as.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**unico**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 