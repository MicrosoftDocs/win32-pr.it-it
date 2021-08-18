---
title: Puntatori univoci
description: Nei programmi C più puntatori possono contenere l'indirizzo dei dati.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adb39d2505daa623f23f47c936fb73d0ecff6e0ad7749c951f9926fd66f33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010994"
---
# <a name="unique-pointers"></a>Puntatori univoci

Nei programmi C più puntatori possono contenere l'indirizzo dei dati. Si dice che i puntatori creano un [*alias*](a-glos.md) per i dati. Gli alias vengono creati anche quando i puntatori puntano a variabili dichiarate. Nel frammento di codice seguente vengono illustrati entrambi i metodi di aliasing:


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



In un tipico programma C è possibile specificare un albero binario usando la definizione seguente:


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



Più puntatori possono accedere al contenuto di un nodo della struttura ad albero. Questa operazione è in genere consigliabile per le applicazioni non distribuite. Tuttavia, questo stile di programmazione genera codice di supporto RPC più complesso. Gli stub client e server richiedono il codice aggiuntivo per gestire i dati e i puntatori. Il codice stub sottostante deve risolvere i vari puntatori agli indirizzi e determinare quale copia dei dati rappresenta la versione più recente.

La quantità di elaborazione può essere ridotta se si garantisce che il puntatore sia l'unico modo in cui l'applicazione può accedere a tale area di memoria. Il puntatore può comunque avere molte delle funzionalità di un puntatore C. Ad esempio, può passare da **valori Null** a valori non **Null** o rimanere uguali. Questa condizione è illustrata nell'esempio seguente. Il puntatore **è Null** prima della chiamata e punta a una stringa valida dopo la chiamata:

![puntatore che cambia tra valori Null e non Null](images/prog-a01.png)

Per impostazione predefinita, il compilatore MIDL applica \[ [l'attributo del](/windows/desktop/Midl/unique) \] puntatore univoco a tutti i puntatori che non sono parametri. Questa impostazione predefinita può essere modificata con \[ [l'attributo predefinito del \_ puntatore.](/windows/desktop/Midl/pointer-default) \]

Un puntatore univoco presenta le caratteristiche seguenti:

-   Può avere il valore **null.**
-   Può passare da **Null** a non **Null** durante la chiamata. Quando il valore viene modificato in diverso da **Null,** al momento della restituzione viene allocata nuova memoria.
-   Può passare da non **Null** a Null **durante** la chiamata. Quando il valore viene modificato **in NULL,** l'applicazione è responsabile del liberare la memoria.
-   Il valore può cambiare da un valore non **Null** a un altro.
-   L'archiviazione a cui punta un puntatore univoco non è accessibile da altri puntatori o nomi nell'operazione.
-   I dati restituiti vengono scritti nella memoria esistente se il puntatore non ha il valore **Null.**

Nell'esempio seguente viene illustrato come definire un puntatore univoco.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

In questo esempio, il *parametro ach* è un puntatore univoco ai dati di tipo carattere che viene inviato a un server da elaborare con la routine RemoteFn.

 

 