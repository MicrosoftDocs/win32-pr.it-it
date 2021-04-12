---
title: length_is (attributo)
description: L'attributo \ length \_ è \ specifica il numero di elementi della matrice da trasmettere. È necessario specificare un valore non negativo.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- attributo length_is MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473043"
---
# <a name="length_is-attribute"></a>lunghezza \_ attributo

L'attributo **\[ length \_ \]** indica il numero di elementi della matrice da trasmettere. È necessario specificare un valore non negativo.

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*elenco di espressioni limitate* 
</dt> <dd>

Specifica una o più espressioni del linguaggio C. Ogni espressione restituisce un valore integer che rappresenta il numero di elementi della matrice da trasmettere. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Separare più espressioni con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ length \_ è \]** determinato dal valore degli indici della matrice corrispondenti all' **\[** [**\_**](last-is.md) **\]** **\[ \_ \]** ultimo attributo is quando non è specificato Last. La relazione tra questi indici di matrice è la seguente: length = Last-First + 1.

La **\[ \_ lunghezza \]** dell'attributo non può essere utilizzata contemporaneamente all'attributo **\[** [**Last \_**](last-is.md) **\]** o **\[** [**String**](string.md) **\]** .

Per definire una stringa calcolata con un valore **\[ length \_ \]** o **\[** [**Last \_ è**](last-is.md) un **\]** attributo, utilizzare una matrice di caratteri o un puntatore senza l' **\[** attributo [**String**](string.md) **\]** .

L'utilizzo di un'espressione costante con la **\[ lunghezza \_ è \]** l'attributo non appropriato dell'attributo. È valido, ma inefficiente, e comporterà il codice di marshalling più lento.

È possibile utilizzare la **\[** [**dimensione \_**](size-is.md) **\]** e la **\[ lunghezza \_ sono \]** gli attributi insieme. Quando si esegue questa operazione, la **\[ dimensione \_ è \]** attributo che controlla la quantità di memoria allocata per i dati. L'attributo **\[ length \_ \]** indica il numero di elementi trasmessi. La quantità di memoria specificata dalla **\[ dimensione \_ è \]** e la **\[ lunghezza \_ è \]** che gli attributi non devono essere uguali. Ad esempio, il client può passare un parametro **\[ in**, **out \]** a un server e specificare un'allocazione di **\[ \_ \] memoria di grandi dimensioni, anche** se specifica un **\[ \_ \]** numero ridotto di elementi di dati da passare con length. Ciò consente al server di riempire la matrice con un numero di dati superiore a quello ricevuto, che può quindi inviare di nuovo al client.

In generale, non è utile specificare le **\[** [**dimensioni \_**](size-is.md) **\]** e la **\[ lunghezza \_ è \]** nei **\[** parametri [**in**](in.md) **\]** o **\[** [**out**](out-idl.md) **\]** . In entrambi i casi, **\[ size \_ \]** controlla l'allocazione di memoria. **\[ \_ È \]** possibile che l'applicazione utilizzi dimensioni per allocare più elementi di matrice rispetto a quanto trasmesso ( **\[ \_ \]** come specificato dalla lunghezza). Tuttavia, questo sarebbe inefficiente. Sarebbe anche inefficiente specificare valori identici per le **\[ dimensioni \_ \]** e la **\[ lunghezza \_ è \]**. Poiché creerebbe un sovraccarico aggiuntivo durante il marshalling del parametro. Quando i valori di **\[ size \_ \]** e **\[ \_ \] length** sono sempre gli stessi, omettere la **\[ lunghezza \_ è \]** Attribute.

## <a name="examples"></a>Esempi

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Attributi di campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ultimo \_ è**](last-is.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[**min \_ è**](min-is.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 