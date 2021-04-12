---
title: parola chiave Union (RPC)
description: Le unioni richiedono parole chiave MIDL speciali per supportarne l'uso con RPC (Remote Procedure Call).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337615"
---
# <a name="union-keyword-rpc"></a>parola chiave Union (RPC)

Alcune funzionalità del linguaggio C, ad esempio le unioni, richiedono parole chiave MIDL speciali per supportarne l'utilizzo nelle chiamate a procedure remote. Un'Unione nel linguaggio C è una variabile che include oggetti di dimensioni e tipi diversi. Lo sviluppatore in genere crea una variabile per tenere traccia dei tipi archiviati nell'Unione. Per funzionare correttamente in un ambiente distribuito, è necessario che la variabile che indica il tipo di Unione, o *discriminante*, sia disponibile anche per il computer remoto. MIDL fornisce il \[ [**\_ tipo di Commuter**](/windows/desktop/Midl/switch-type) \] e \[ [**Switch \_ è**](/windows/desktop/Midl/switch-is) \] keywords per identificare il tipo e il nome discriminante.

MIDL richiede che il discriminante venga trasmesso con l'Unione in uno dei due modi seguenti:

-   L'Unione e discriminante devono essere specificati come parametri.
-   L'Unione e discriminante devono essere inclusi in un pacchetto in una struttura.

Due tipi fondamentali di unioni discriminate vengono forniti da MIDL: [**unincapsulated \_**](/windows/desktop/Midl/nonencapsulated-unions) Union e incapsulated [**\_ Union**](/windows/desktop/Midl/encapsulated-unions). Il discriminante di un'Unione non incapsulata è un altro parametro se l'Unione è un parametro. Si tratta di un altro campo se l'Unione è un campo di una struttura. La definizione di un'Unione incapsulata viene trasformata in una definizione di struttura il cui primo campo è discriminante e il cui secondo e l'ultimo campo sono l'Unione. Nell'esempio seguente viene illustrato come fornire i parametri Union e discriminante:

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

L'Unione nell'esempio precedente può contenere un solo valore, ovvero **short**, **float** o **char**. La definizione del tipo per l'Unione include l'attributo del **\_ tipo di opzione** MIDL che specifica il tipo di discriminante. Qui, \[ Switch \_ Type (Short) \] specifica che discriminante è di tipo **short**. L'opzione deve essere un tipo Integer.

Se l'Unione è un membro di una struttura, discriminante deve essere un membro della stessa struttura. Se l'Unione è un parametro, discriminante deve essere un altro parametro. Il prototipo per la funzione **UnionParamProc** nell'esempio precedente mostra discriminante *sUtype* come ultimo parametro della chiamata. (Discriminante può essere visualizzato in qualsiasi posizione nella chiamata). Il tipo del parametro specificato nell' **\[ opzione \_ è \]** l'attributo deve corrispondere al tipo specificato nell'attributo **\[ Switch \_ Type \]** .

Nell'esempio seguente viene illustrato l'utilizzo di una singola struttura che fornisce il pacchetto di discriminante con l'Unione:

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

Il compilatore MIDL Microsoft RPC consente le dichiarazioni Union all'esterno dei costrutti [**typedef**](/windows/desktop/Midl/typedef) . Questa funzionalità è un'estensione di DCE IDL. Per ulteriori informazioni, vedere [**Unione**](/windows/desktop/Midl/union).

 

 