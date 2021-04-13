---
title: callback (attributo)
description: L'attributo \ callback \ dichiara una funzione di callback statica esistente sul lato client dell'applicazione distribuita. Le funzioni di callback consentono al server di eseguire il codice sul client.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- attributo di callback MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398961"
---
# <a name="callback-attribute"></a>callback (attributo)

L'attributo **\[ callback \]** dichiara una funzione di callback statica esistente sul lato client dell'applicazione distribuita. Le funzioni di callback consentono al server di eseguire il codice sul client.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Function-attr-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**local**](local.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e gli attributi Usage **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md) **\]** . Separare più attributi con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [ \_ tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*PTR-dichiaratore* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*elenco attributi* 
</dt> <dd>

Specifica zero o più attributi direzionali, attributi di campo, attributi di utilizzo e attributi del puntatore appropriati per il tipo di parametro specificato. Separare più attributi con virgole.

</dd> <dt>

*dichiaratore* 
</dt> <dd>

Specifica un dichiaratore C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). L'identificatore del nome del parametro è facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione di **\[ callback \]** è utile quando il server deve ottenere informazioni dal client. Se le applicazioni server sono supportate in Windows 3. *x*, il server può effettuare una chiamata a una procedura remota in Windows 3. Server *x* per ottenere le informazioni necessarie. La funzione di callback ha lo stesso scopo e consente al server di eseguire una query sul client per ottenere informazioni nel contesto della chiamata originale.

I callback sono casi speciali di chiamate remote eseguite come parte di un singolo thread. Viene emesso un callback nel contesto di una chiamata remota. Qualsiasi procedura remota definita come parte della stessa interfaccia della funzione di callback statica può chiamare la funzione di callback.

È importante notare che l'uso del \[ callback \] non è consigliato nella programmazione multithread. Come funzione di programmazione a thread singolo, non è disponibile per supportare le richieste di sicurezza offerte da un ambiente multithread.

Impossibile utilizzare la funzione **RpcCancelThread** per annullare una chiamata che può inviare un callback statico. Se una particolare chiamata a una procedura remota non comporterà mai un callback, può essere annullata. In caso contrario, una chiamata può essere annullata solo se è possibile garantire che non sia stato emesso un callback per esso.

Solo le sequenze orientate alla connessione e del protocollo locale supportano l'attributo callback. La dimensione dei \[ dati out \] per i callback sulla sequenza del protocollo locale è limitata a 150 byte. Se un'interfaccia RPC usa una sequenza di protocollo senza connessione (datagramma), le chiamate a procedure con l'attributo di callback avranno esito negativo.

Non è possibile utilizzare gli handle come parametri nelle funzioni di callback. Poiché i callback vengono sempre eseguiti nel contesto di una chiamata, l'handle di associazione utilizzato dal client per effettuare la chiamata al server viene utilizzato anche come handle di binding dal server al client.

I callback possono annidarsi in qualsiasi profondità.

## <a name="examples"></a>Esempi

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 