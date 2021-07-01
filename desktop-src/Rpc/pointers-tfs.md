---
title: Puntatori (RPC)
description: Informazioni su un puntatore comune RPC, definito come qualsiasi elemento diverso da puntatori a interfaccia e puntatori al conteggio dei byte.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119706"
---
# <a name="pointers-rpc"></a>Puntatori (RPC)

## <a name="common-pointers"></a>Puntatori comuni

Un puntatore comune è definito come qualsiasi elemento diverso da puntatori a interfaccia e puntatori al conteggio dei byte.

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

Il primo formato viene usato se il puntatore è un puntatore a un tipo semplice o a un puntatore di stringa non di tipo grande. Il secondo formato viene usato per i puntatori a tutti gli altri tipi. Gli attributi del puntatore indicano il layout della descrizione con il \_ flag FC SIMPLE \_ POINTER.

Il \_ tipo di<1> è uno dei seguenti.



| Formatta carattere | Descrizione                              |
|------------------|------------------------------------------|
| FC \_ RP           | Puntatore di riferimento.                     |
| FC \_ UP           | Puntatore univoco.                        |
| FC \_ FP           | Puntatore completo.                          |
| FC \_ OP           | Puntatore univoco in un'interfaccia oggetto. |



 

Il motivo per distinguere FC OP è semantico: nelle interfacce oggetto, un puntatore in uscita deve essere liberato prima di eseguire \_ l'unmarsshaling di un nuovo oggetto e assegnare un nuovo valore del \[ \] puntatore.

Gli \_ attributi<1> possono avere uno qualsiasi dei flag illustrati nella tabella seguente.



| Attributo | Flag              | Descrizione                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC \_ ALLOCATE \_ ALL \_ NODES | Il puntatore fa parte di uno schema di allocazione allocate(tutti \_ i nodi).                                                                                                                                                                   |
| 02   | FC \_ DONT \_ FREE           | Puntatore allocate(don't \_ free).                                                                                                                                                                                                      |
| 04   | FC \_ ALLOCED \_ ON \_ STACK   | Puntatore il cui riferimento viene allocato nello stack dello stub.                                                                                                                                                                            |
| 08   | PUNTATORE \_ FC \_ SEMPLICE      | Puntatore a un tipo semplice o a una stringa non conforme. Questo flag impostato indica il layout della descrizione del puntatore come layout del puntatore semplice descritto in precedenza. In caso contrario, viene indicato il formato del descrittore con l'offset. |
| 10   | DEREF \_ \_ PUNTATORE FC       | Puntatore che deve essere dereferenziato prima di gestire il riferimento del puntatore.                                                                                                                                                           |



 

I puntatori con size \_ is(), max \_ is(), length \_ is(), last \_ is() e/o first is() applicati hanno descrizioni di stringa di formato identiche a un puntatore a una matrice del tipo appropriato \_ (ad esempio, \_ \_ una matrice conforme se size is() viene applicato, una matrice variabile conforme se size is() e length viene \_ applicato).

## <a name="interface-pointers"></a>Puntatori a interfaccia

Una stringa di formato del puntatore a interfaccia a oggetti ha uno dei due formati seguenti, a seconda che l'IID corrispondente sia noto al compilatore.

Un puntatore a interfaccia con un IID costante ha la descrizione seguente:

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

L'iid<16> parte è l'IID effettivo per il puntatore di interfaccia. L'iid viene scritto nella stringa di formato in un formato identico alla struttura dei dati GUID: long, short, short, char \[ 8 \] .

La descrizione di un puntatore a interfaccia con iid \_ is() applicata è:

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

La descrizione iid<> descrittore di correlazione e ha 4 o 6 byte a seconda che \_ [**/robust**](/windows/desktop/Midl/-robust) sia o meno utilizzato. Il valore calcolato dalla **funzione NdrComputeConformance** è il puntatore IID.

## <a name="byte-count-pointers"></a>Puntatori di conteggio byte

I puntatori al conteggio dei byte sono correlati a uno speciale attributo di ottimizzazione denominato \[ **byte \_ count** \] . Vengono usati i formati seguenti:

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

–and:

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

La descrizione del<> byte è un descrittore di correlazione e ha 4 o 6 byte a seconda che \_ \_ [**/robust**](/windows/desktop/Midl/-robust) sia o meno utilizzato.

La descrizione \_<> pointee è una descrizione del tipo pointee.

 

 
