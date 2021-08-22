---
title: size_is (attributo)
description: Usare l'attributo \ size is\ per specificare la dimensione della memoria, in elementi, allocata per i puntatori ridimensionati, i puntatori ridimensionati ai puntatori ridimensionati e le matrici \_ multidimensionali o singole.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is attributo MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd57748d3ad92407fd65f3a6af7fc1ebb68321b576d57a50b6ba6f5546f8d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066701"
---
# <a name="size_is-attribute"></a>size \_ è attribute

Usare \[ **l'attributo size \_ is** per specificare la dimensione della memoria, in elementi, allocata per puntatori ridimensionati, puntatori ridimensionati a puntatori ridimensionati e matrici singole o \] multidimensionali.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Specifica una o più espressioni in linguaggio C. Ogni espressione restituisce un intero non negativo che rappresenta la quantità di memoria allocata a un puntatore ridimensionato o a una matrice. Nel caso di una matrice, specifica una singola espressione che rappresenta la dimensione di allocazione, in elementi, della prima dimensione della matrice. Il compilatore MIDL supporta espressioni condizionali, logiche, relazionali ed aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Usare le virgole come segnaposto per i parametri impliciti o per separare più espressioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si usa l'attributo size is per allocare memoria per una matrice multidimensionale e si usa la notazione di matrice, tenere presente che solo la prima dimensione di una matrice \[ **\_** \] \[ multidimensionale può essere determinata dinamicamente in fase di \] esecuzione. Le altre dimensioni devono essere specificate in modo statico. Per altre informazioni sull'uso dell'attributo size is con più livelli di puntatori per consentire a un server di restituire una matrice di dati ridimensionata dinamicamente a un client, come illustrato nell'esempio Proc7, vedere Più livelli di \[ **\_** \] [puntatori.](/windows/desktop/Rpc/multiple-levels-of-pointers)

È possibile usare \[ **size \_ is** o \] max [**\_ is**](max-is.md) (ma non entrambi nello stesso elenco di attributi) per specificare le dimensioni di una matrice i cui limiti superiori vengono determinati in fase di esecuzione. Si noti, tuttavia, che \[ **\_ l'attributo size non** può essere usato nelle dimensioni di matrice \] fisse. \[ **L'attributo max \_ is** \] specifica l'indice di matrice massimo valido. Di conseguenza, specificare \[ size \_ is(n) equivale a specificare max \] \[ \_ is(n-1) \] .

Un \[ [**parametro in**](in.md) \] o in out \[ [](out-idl.md) \] conformant-array \[ [](string.md) \] \[ **\_** \] \[ [**\_**](max-is.md) con \] l'attributo string non deve avere l'attributo size is o max is. In questo caso, la dimensione dell'allocazione è determinata dal carattere di terminazione NULL della stringa di input. Tutte le altre matrici conformi con \[ l'attributo string devono avere un attributo size \] \[ **\_ is** \] o max \[ **\_ is.** \]

Sebbene sia valido usare l'attributo \[ **size \_ is** \] con una costante, questa operazione è inefficiente e non necessaria. Ad esempio, usare una matrice di dimensioni fisse:

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

invece di:

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

È possibile usare la \[ **dimensione è \_ e** \] la lunghezza è \[ [**\_ attributi**](length-is.md) \] insieme. Quando si esegue questa operazione, \[ **\_ l'attributo size controlla** la quantità di memoria \] allocata per i dati. \[ **\_ L'attributo length** specifica il numero di elementi \] trasmessi. La quantità di memoria specificata dalla dimensione \[ **\_ è** \] e la lunghezza \[ **\_ è** \] che gli attributi non devono essere uguali. Ad esempio, il client può passare un parametro in,out a un server e specificare un'allocazione di memoria di grandi dimensioni con dimensioni pari a , anche se specifica un numero ridotto di elementi dati da passare con lunghezza \[ \] è \[ **\_** \] \[ **\_** \] . In questo modo il server può riempire la matrice con più dati di quelli ricevuti, che può quindi inviare di nuovo al client.

In generale, non è utile specificare che le dimensioni \[ **\_ sono** e la \] lunghezza \[ [**\_ è**](length-is.md) \] impostata sui parametri in \[ o \] \[ \] out. In entrambi i casi, \[ **size è controlla \_ l'allocazione** \] di memoria. L'applicazione potrebbe \[ **usare le dimensioni \_ per** allocare più elementi di matrice di quanto \] trasm. Come specificato da length \[ **\_ è** \] . Tuttavia, ciò sarebbe inefficiente. Sarebbe inoltre inefficiente specificare valori identici per \[ **size \_ e** \] length \[ **\_ è** \] . Si creerebbe un sovraccarico aggiuntivo durante il marshalling dei parametri. Se i valori di \[ **size sono \_ e** \] length \[ **\_ è** \] sempre lo stesso, omettere \[ **l'attributo length \_ is.** \]

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

[**Matrici**](arrays-1.md)
</dt> <dt>

[Attributi di campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**first \_ è**](first-is.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**last \_ is**](last-is.md)
</dt> <dt>

[**length \_ è**](length-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**min \_ is**](min-is.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 