---
title: size_is (attributo)
description: Usare l'attributo \ size \_ is \ per specificare le dimensioni della memoria, negli elementi, allocati per i puntatori dimensionati, i puntatori dimensionati ai puntatori dimensionati e le matrici mono o multidimensionali.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- attributo size_is MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724946"
---
# <a name="size_is-attribute"></a>size \_ è un attributo

Usare l' \[ attributo **size \_ è** \] per specificare la dimensione della memoria, in elementi, allocata per i puntatori dimensionati, i puntatori dimensionati ai puntatori di dimensione e le matrici mono o multidimensionali.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*elenco di espressioni limitate* 
</dt> <dd>

Specifica una o più espressioni del linguaggio C. Ogni espressione restituisce un numero intero non negativo che rappresenta la quantità di memoria allocata a un puntatore di dimensioni o una matrice. Nel caso di una matrice, specifica una singola espressione che rappresenta la dimensione di allocazione, in elementi, della prima dimensione della matrice. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Utilizzare le virgole come segnaposto per i parametri impliciti o per separare più espressioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si utilizza la \[ **dimensione \_ è** \] attributo per allocare memoria per una matrice multidimensionale e si utilizza la \[ \] notazione di matrice, tenere presente che solo la prima dimensione di una matrice multidimensionale può essere determinata in modo dinamico in fase di esecuzione. Le altre dimensioni devono essere specificate in modo statico. Per ulteriori informazioni sull'utilizzo delle \[ **dimensioni \_ è** \] attributo con più livelli di puntatori per consentire a un server di restituire una matrice di dati di dimensioni dinamiche a un client, come illustrato nell'esempio Proc7, vedere [più livelli di puntatori](/windows/desktop/Rpc/multiple-levels-of-pointers).

È possibile utilizzare le \[ **dimensioni \_** \] oppure il valore [**Max \_ è**](max-is.md) (ma non entrambi nello stesso elenco di attributi) per specificare le dimensioni di una matrice i cui limiti superiori vengono determinati in fase di esecuzione. Si noti, tuttavia, che la \[ **dimensione \_ è** \] attributo non può essere utilizzata sulle dimensioni della matrice fisse. L' \[ attributo **Max \_ is** \] specifica l'indice di matrice valido massimo. Di conseguenza, se si specifica \[ size \_ è (n) \] equivale a specificare \[ Max \_ è (n-1) \] .

Un oggetto \[ [**in**](in.md) \] o \[ in, [**out**](out-idl.md) \] conforme-il parametro della matrice con l' \[ attributo [**stringa**](string.md) \] non deve avere la \[ **dimensione \_ è** \] o \[ [**Max \_ è**](max-is.md) \] Attribute. In questo caso, la dimensione dell'allocazione è determinata dal carattere di terminazione NULL della stringa di input. Tutte le altre matrici conformi con l' \[ \] attributo stringa devono avere una \[ **dimensione \_** oppure il valore \] \[ **massimo \_ è** \] attributo.

Sebbene sia possibile utilizzare la \[ **dimensione \_ è** l' \] attributo con una costante, questa operazione non è efficiente e non è necessaria. Ad esempio, usare una matrice a dimensione fissa:

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

invece di:

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

È possibile utilizzare la \[ **dimensione \_** \] e la \[ [**lunghezza \_ sono**](length-is.md) \] gli attributi insieme. Quando si esegue questa operazione, la \[ **dimensione \_ è** \] attributo che controlla la quantità di memoria allocata per i dati. L' \[ **attributo \_ length** \] indica il numero di elementi trasmessi. La quantità di memoria specificata dalla \[ **dimensione \_ è** \] e la \[ **lunghezza \_ è** che \] gli attributi non devono essere uguali. Ad esempio, il client può passare un \[ parametro in, out \] a un server e specificare un'allocazione di memoria di grandi dimensioni \[ **\_** \] , anche se specifica un numero ridotto di elementi di dati da passare con \[ **length \_** \] . Ciò consente al server di riempire la matrice con un numero di dati superiore a quello ricevuto, che può quindi inviare di nuovo al client.

In generale, non è utile specificare le \[ **\_ dimensioni** \] e la \[ [**lunghezza \_ è**](length-is.md) nei \] \[ parametri in \] o \[ out \] . In entrambi i casi, \[ **size \_** \] Controlla l'allocazione di memoria. È possibile che l'applicazione utilizzi \[ **dimensioni \_** \] per allocare più elementi di matrice rispetto a quanto trasmesso (come specificato dalla \[ **lunghezza \_** \] ). Tuttavia, questo sarebbe inefficiente. Sarebbe anche inefficiente specificare valori identici per \[ le **dimensioni e \_** la \] \[ **lunghezza \_ è** \] . Creerebbe un sovraccarico aggiuntivo durante il marshalling del parametro. Se i valori di \[ **size \_** \] e \[ **length \_** \] sono sempre uguali, omettere la \[ **lunghezza \_ è** \] Attribute.

## <a name="examples"></a>Esempi

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Attributi di campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**ultimo \_ è**](last-is.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[**min \_ è**](min-is.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 