---
title: call_as (attributo)
description: L'attributo \ Call \_ As \ consente di eseguire il mapping di una funzione che non può essere chiamata in modalità remota a una funzione remota.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- attributo call_as MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299211"
---
# <a name="call_as-attribute"></a>chiama \_ come attributo

L'attributo **\[ Call \_ As \]** consente di eseguire il mapping di una funzione che non può essere chiamata in modalità remota a una funzione remota.

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*local-proc* 
</dt> <dd>

Specifica una routine definita dall'operazione.

</dd> <dt>

*operazione-attributo-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano all'operazione. Separare più attributi con virgole.

</dd> <dt>

*nome operazione* 
</dt> <dd>

Specifica l'operazione denominata presentata all'applicazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La possibilità di eseguire il mapping di una funzione che non può essere chiamata in modalità remota a una funzione remota è particolarmente utile nelle interfacce con numerosi tipi di parametro che non possono essere trasmessi attraverso la rete. Anziché utilizzare molti tipi di **\[** [**rappresentazione \_**](represent-as.md) **\]** e **\[** [**trasmissione \_ come**](transmit-as.md) **\]** tipi, è possibile combinare tutte le conversioni utilizzando la **\[ chiamata \_ come \]** routine. Si forniscono le due chiamate **\[ \_ come \]** routine (lato client e lato server) per associare la routine tra le chiamate dell'applicazione e le chiamate remote.

La **\[ chiamata \_ come \]** attributo può essere usata per le interfacce oggetto. In questo caso, la definizione dell'interfaccia può essere usata per le chiamate locali e per le chiamate remote perché **\[ Call \_ As \]** consente a un'interfaccia a cui non è possibile accedere in modalità remota di essere mappata in modo trasparente a un'interfaccia remota. Impossibile utilizzare la **\[ chiamata \_ come \]** attributo con la modalità [**/OSF**](-osf.md) .

Si supponga, ad esempio, che la routine **F1** nell'interfaccia oggetto **IFace** richieda numerose conversioni tra le chiamate utente e ciò che viene effettivamente trasmesso. Gli esempi seguenti descrivono i file IDL e ACF per l'interfaccia **IFace**:

Nel file IDL per l'interfaccia **IFace**:

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

In ACF per l'interfaccia **IFace**:

``` syntax
[call_as( f1 )] Remf1();
```

In questo modo il file di intestazione generato definisce l'interfaccia utilizzando la definizione **F1**, ma fornisce anche stub per **Remf1**.

Il compilatore MIDL genererà il seguente vtable nel file di intestazione per l'interfaccia **IFace**:

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

Il proxy sul lato client avrà quindi un tipico proxy generato da MIDL per **Remf1**, mentre lo stub del lato server per **Remf1** sarà lo stesso dello stub tipico generato da MIDL:

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

Quindi, le due **\[ chiamate \_ come \] routine di** vincolo (lato client e lato server) devono essere codificate manualmente:

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

Per le interfacce oggetto, si tratta dei prototipi per le routine di vincolo.

Per lato client:

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

Per lato server:

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

Per le interfacce non oggetto, si tratta dei prototipi per le routine di vincolo.

Per lato client:

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

Per lato server:

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**rappresenta \_ come**](represent-as.md)
</dt> <dt>

[**Trasmetti \_ come**](transmit-as.md)
</dt> </dl>

 

 




