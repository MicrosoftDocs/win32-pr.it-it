---
title: Puntatori (RPC)
description: Pointers
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cabf5109506bc1e194a39c809bfb43a8f952fbf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118758"
---
# <a name="pointers-rpc"></a>Puntatori (RPC)

## <a name="common-pointers"></a>Puntatori comuni

Un puntatore comune è definito come tutto tranne i puntatori di interfaccia e i puntatori di conteggio dei byte.

Esistono due possibili layout per la descrizione:

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

–oppure–

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

Il primo formato viene usato se il puntatore è un puntatore a un tipo semplice o a un puntatore di stringa non ridimensionato. Il secondo formato viene usato per i puntatori a tutti gli altri tipi. Gli attributi del puntatore indicano il layout della descrizione con il \_ flag del puntatore semplice FC \_ .

\_il tipo di puntatore<1> è uno dei seguenti.



| Formato carattere | Descrizione                              |
|------------------|------------------------------------------|
| \_RP FC           | Puntatore di riferimento.                     |
| FC \_ attivo           | Puntatore univoco.                        |
| \_FP FC           | Puntatore completo.                          |
| \_op FC           | Puntatore univoco in un'interfaccia dell'oggetto. |



 

Il motivo per distinguere FC \_ op è semantico: nelle interfacce oggetto, un \[ puntatore out \] deve essere liberato prima di eseguire l'unmarshalling di un nuovo oggetto e l'assegnazione di un nuovo valore del puntatore.

Gli \_ attributi del puntatore<1> possono avere uno dei flag mostrati nella tabella seguente.



| Flag | Descrizione              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC \_ allocare \_ tutti i \_ nodi | Il puntatore è parte di uno schema di allocazione (tutti i \_ nodi).                                                                                                                                                                   |
| 02   | FC \_ non \_ disponibile           | Puntatore allocate (non \_ gratuito).                                                                                                                                                                                                      |
| 04   | \_allocati FC \_ nello \_ stack   | Puntatore il cui referente viene allocato nello stack dello stub.                                                                                                                                                                            |
| 08   | \_puntatore semplice \_ FC      | Puntatore a un tipo semplice o a una stringa conforme non dimensionata. Questo flag impostato indica il layout della descrizione del puntatore come il layout del puntatore semplice descritto in precedenza; in caso contrario, viene indicato il formato del descrittore con l'offset. |
| 10   | \_Deref puntatore \_ FC       | Puntatore che deve essere dereferenziato prima di gestire il referente del puntatore.                                                                                                                                                           |



 

I puntatori con dimensione \_ è (), il valore Max \_ è (), length \_ è (), Last \_ è () e/o First \_ is () viene applicato a tali stringhe di formato identico a un puntatore a una matrice del tipo appropriato (ad esempio, una matrice conforme se size \_ is () viene applicato, una matrice variabile conforme se size \_ è () e \_ viene applicata la lunghezza.

## <a name="interface-pointers"></a>Puntatori a interfaccia

Una stringa di formato puntatore a interfaccia a oggetti presenta uno dei due formati, a seconda che l'IID corrispondente sia noto al compilatore.

Un puntatore di interfaccia con un IID costante presenta la descrizione seguente:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

L'IID<16> parte è l'IID effettivo per il puntatore di interfaccia. L'IID viene scritto nella stringa di formato in un formato identico alla struttura di dati GUID: Long, short, short, char \[ 8 \] .

Viene applicata la descrizione di un puntatore a interfaccia con IID \_ ():

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

La descrizione dell'IID \_<> è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) . Il valore calcolato dalla funzione **NdrComputeConformance** è il puntatore IID.

## <a name="byte-count-pointers"></a>Puntatori conteggio byte

I puntatori al numero di byte sono correlati a un attributo di ottimizzazione speciale denominato \[ **\_ conteggio byte** \] . Vengono usati i formati seguenti:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

e

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

La descrizione del conteggio dei byte \_ \_<> è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .

La descrizione del puntatore \_<> è una descrizione del tipo di puntatore.

 

 
