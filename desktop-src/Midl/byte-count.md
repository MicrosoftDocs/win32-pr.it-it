---
title: byte_count attributo
description: L'attributo \ byte count\ ACF è un attributo di parametro che associa una \_ dimensione, in byte, all'area di memoria indicata dal puntatore.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count attributo MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffd42e27be4768fc0817aa76bb366429e236b3a82c45d081a05485b8520a23a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807824"
---
# <a name="byte_count-attribute"></a>Attributo \_ byte count

**\[ \_ L'attributo \]** ACF conteggio byte è un attributo di parametro che associa una dimensione, in byte, all'area di memoria indicata dal puntatore.

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Specifica zero o più attributi della funzione ACF.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione definita nel file IDL. Il nome della funzione è obbligatorio.

</dd> <dt>

*length-variable-name* 
</dt> <dd>

Specifica il nome del [**\[ parametro in \]**](in.md)-only che specifica le dimensioni, in byte, dell'area di memoria a cui fa riferimento *parameter-name*.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Specifica il nome del parametro del puntatore [**\[ out \]**](out-idl.md)-only definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il numero di **\[ byte dell'attributo \_ \]** ACF rappresenta un'estensione Microsoft per DCE IDL. Pertanto, questo attributo non è disponibile quando si usa l'opzione del compilatore MIDL [**/osf**](-osf.md).

> [!Note]  
> **\[ L'attributo \] byte count** non è più supportato nella sintassi NDR64 a causa della difficoltà di stima delle dimensioni necessarie per tutti i parametri [**\[ out. \]**](out-idl.md)

 

La memoria a cui fa riferimento il parametro pointer è contigua e non viene allocata o liberata dagli stub client. Questa funzionalità dell'attributo **\[ \_ byte count \]** consente di creare un'area del buffer permanente nella memoria client che può essere riutilizzata durante più chiamate alla procedura remota.

La possibilità di disattivare l'allocazione di memoria stub client consente di ottimizzare l'applicazione per l'efficienza. Ad esempio, **\[ l'attributo byte \_ count \]** può essere usato dalle funzioni del provider di servizi che usano Microsoft RPC. Quando un'applicazione utente chiama l'API del provider di servizi e invia un puntatore a un buffer, il provider di servizi può passare il puntatore del buffer alla funzione remota. Il provider di servizi può riutilizzare il buffer durante più chiamate remote senza forzare l'utente a riallocare l'area di memoria.

L'area di memoria può contenere strutture di dati complesse costituite da più puntatori. Poiché l'area di memoria è contigua, l'applicazione non deve eseguire diverse chiamate per liberare singolarmente ogni puntatore e ogni struttura. Può invece allocare o liberare l'area di memoria con una chiamata all'allocazione di memoria o alla routine free.

Il buffer deve essere un [**\[ parametro \] out-only,**](out-idl.md)mentre la lunghezza del buffer in byte deve essere un parametro [**\[ in \]**](in.md)-only.

Specificare un buffer sufficientemente grande da contenere tutti i [**\[ parametri out. \]**](out-idl.md) A causa della spaziatura interna nascosta, usare valori sovrastimati anziché conteggi esatti. Ad esempio, i puntatori a 4 byte vengono disassociati su un limite allineato a 4 byte su piattaforme a 32 bit e puntatori a 8 byte su un limite a 8 byte su piattaforme a 64 bit. Di conseguenza, la spaziatura interna dell'allineamento che verranno eseguono gli stub deve essere contabilata nello spazio per il buffer. Inoltre, i livelli di pacchetto usati durante la compilazione del linguaggio C possono variare. Usare un valore di conteggio byte che conti per i byte di pacchetto aggiuntivi aggiunti per il livello di pacchetto usato durante la compilazione del linguaggio C. Una procedura sicura che copre sia le piattaforme a 32 bit che le piattaforme a 64 bit consiste nel presupporre che ogni oggetto che entra nel blocco di memoria grande inizi da un indirizzo multiplo di 8.

## <a name="examples"></a>Esempi

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**length \_ è**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**size \_ è**](size-is.md)
</dt> </dl>

 

 




