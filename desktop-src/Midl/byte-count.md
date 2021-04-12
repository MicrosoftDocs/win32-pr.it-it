---
title: attributo byte_count
description: L'attributo \ byte \_ count \ ACF è un attributo di parametro che associa una dimensione, in byte, all'area di memoria indicata dal puntatore.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- attributo byte_count MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334428"
---
# <a name="byte_count-attribute"></a>byte \_ Count (attributo)

L'attributo di **\[ \_ numero \] di byte** ACF è un attributo di parametro che associa una dimensione, in byte, all'area di memoria indicata dal puntatore.

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi della funzione ACF.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione definita nel file IDL. Il nome della funzione è obbligatorio.

</dd> <dt>

*nome-variabile-lunghezza* 
</dt> <dd>

Specifica il nome del parametro [**\[ in \]**](in.md)-only che specifica la dimensione, in byte, dell'area di memoria a cui fa riferimento il *parametro-Name*.

</dd> <dt>

*Nome parametro* 
</dt> <dd>

Specifica il nome del parametro del puntatore di sola [**\[ uscita \]**](out-idl.md)definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **\[ \_ numero \] di byte** dell'attributo ACF rappresenta un'estensione Microsoft per DCE IDL. Pertanto, questo attributo non è disponibile quando si usa l'opzione del compilatore MIDL [**/OSF**](-osf.md).

> [!Note]  
> L'attributo **\[ Count \] byte** non è più supportato nella sintassi NDR64 a causa della difficoltà di stima delle dimensioni necessarie per tutti i parametri [**\[ out \]**](out-idl.md) .

 

La memoria a cui fa riferimento il parametro puntatore è contigua e non viene allocata o liberata dagli stub client. Questa funzionalità dell'attributo **\[ \_ conteggio \] byte** consente di creare un'area buffer permanente nella memoria client che può essere riutilizzata durante più di una chiamata alla procedura remota.

La possibilità di disattivare l'allocazione di memoria stub client consente di ottimizzare l'applicazione per l'efficienza. Ad esempio, l'attributo **\[ \_ conteggio \] byte** può essere usato dalle funzioni del provider di servizi che usano Microsoft RPC. Quando un'applicazione utente chiama l'API del provider di servizi e invia un puntatore a un buffer, il provider di servizi può passare il puntatore del buffer alla funzione remota. Il provider di servizi può riutilizzare il buffer durante più chiamate remote senza forzare l'utente a riallocare l'area di memoria.

L'area di memoria può contenere strutture di dati complesse costituite da più puntatori. Poiché l'area di memoria è contigua, l'applicazione non deve effettuare diverse chiamate per liberare singolarmente ogni puntatore e struttura. Al contrario, può allocare o liberare l'area di memoria con una sola chiamata all'allocazione di memoria o alla routine gratuita.

Il buffer deve essere un parametro di sola [**\[ uscita \]**](out-idl.md), mentre la lunghezza del buffer in byte deve essere un parametro solo [**\[ in \]**](in.md).

Specificare un buffer sufficientemente grande da contenere tutti i parametri [**\[ out \]**](out-idl.md) . A causa della spaziatura interna nascosta, utilizzare le sovrastime anziché i conteggi esatti. Ad esempio, i puntatori a 4 byte vengono sottoposti a unmarshalling su un limite allineato a 4 byte su piattaforme a 32 bit e puntatori a 8 byte su un limite di 8 byte su piattaforme a 64 bit. La spaziatura interna dell'allineamento che verrà eseguita dagli Stub deve pertanto essere rappresentata nello spazio per il buffer. Inoltre, i livelli di compressione utilizzati durante la compilazione in linguaggio C possono variare. Usare un valore di conteggio byte che conti per i byte di compressione aggiuntivi aggiunti per il livello di compressione usato durante la compilazione in linguaggio C. Una procedura sicura che copre entrambe le piattaforme a 32 bit e le piattaforme a 64 bit consiste nel presupposto che ogni oggetto che entra nel blocco di memoria grande inizi a un indirizzo che è un multiplo di 8.

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

[**in**](in.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> </dl>

 

 




