---
title: attributo callback
description: L'attributo \ callback\ dichiara una funzione di callback statica presente sul lato client dell'applicazione distribuita. Le funzioni di callback consentono al server di eseguire codice nel client.
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
ms.openlocfilehash: e77eb93a78553ccbc95b1671dc215012eeccc56b0bff8ea23e47f68aaf51e10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807337"
---
# <a name="callback-attribute"></a>attributo callback

**\[ L'attributo \]** di callback dichiara una funzione di callback statica presente sul lato client dell'applicazione distribuita. Le funzioni di callback consentono al server di eseguire codice nel client.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*function-attr-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono locali, l'attributo puntatore ref , unique o ptr e la stringa degli attributi di utilizzo **\[** [](local.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** , **\[** [](string.md) **\]** **\[** [**ignora**](ignore.md) **\]** e **\[** [**l'handle di \_ contesto**](context-handle.md) **\]** . Separare più attributi con virgole.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo [di \_ base,](midl-base-types.md) [**uno struct,**](struct.md) [**un'unione,**](union.md) [**un tipo enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*ptr-declarator* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore di puntatore usato in C; viene costruito \* dall'designatore , dai modificatori come **far** e dal qualificatore [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Specifica zero o più attributi direzionali, attributi di campo, attributi di utilizzo e attributi del puntatore appropriati per il tipo di parametro specificato. Separare più attributi con virgole.

</dd> <dt>

*Dichiaratore* 
</dt> <dd>

Specifica un dichiaratore C standard, ad esempio identificatori, dichiaratori di puntatori e dichiaratori di matrice. Per altre informazioni, vedere [Matrici e Sized-Pointer,](array-and-sized-pointer-attributes.md) [**matrici**](arrays-1.md)e [matrici e puntatori.](/windows/desktop/Rpc/arrays-and-pointers) L'identificatore del nome del parametro è facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\[ funzione di callback \]** è utile quando il server deve ottenere informazioni dal client. Se le applicazioni server sono supportate in Windows 3. *x*, il server può effettuare una chiamata a una procedura remota nel Windows 3. *x* server per ottenere le informazioni necessarie. La funzione di callback ha lo stesso scopo e consente al server di eseguire una query sul client per ottenere informazioni nel contesto della chiamata originale.

I callback sono casi speciali di chiamate remote eseguite come parte di un singolo thread. Un callback viene generato nel contesto di una chiamata remota. Qualsiasi procedura remota definita come parte della stessa interfaccia della funzione di callback statica può chiamare la funzione di callback.

È importante notare che l'uso del \[ callback non è consigliato nella programmazione \] multi-thread. Come funzione di programmazione a thread singolo, non è in grado di supportare le richieste di sicurezza fornite da un ambiente multi-thread.

La **funzione RpcCancelThread** non può essere usata per annullare una chiamata che può inviare un callback statico. Se una particolare chiamata di procedura remota non comporta mai un callback, può essere annullata. In caso contrario, una chiamata può essere annullata solo se è possibile garantire che non sia stato emesso un callback per tale chiamata.

Solo le sequenze orientate alla connessione e del protocollo locale supportano l'attributo di callback . La dimensione dei dati out per i callback sulla sequenza del protocollo \[ locale è limitata a \] 150 byte. Se un'interfaccia RPC usa una sequenza di protocollo senza connessione (datagramma), le chiamate alle routine con l'attributo di callback avranno esito negativo.

Gli handle non possono essere usati come parametri nelle funzioni di callback. Poiché i callback vengono sempre eseguiti nel contesto di una chiamata, l'handle di associazione utilizzato dal client per effettuare la chiamata al server viene usato anche come handle di associazione dal server al client.

I callback possono annidare fino a qualsiasi profondità.

## <a name="examples"></a>Esempi

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorare**](ignore.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 