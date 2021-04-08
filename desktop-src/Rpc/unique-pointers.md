---
title: Puntatori univoci
description: Nei programmi C, più di un puntatore può contenere l'indirizzo dei dati.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046780"
---
# <a name="unique-pointers"></a>Puntatori univoci

Nei programmi C, più di un puntatore può contenere l'indirizzo dei dati. Ai puntatori viene detto di creare un [*alias*](a-glos.md) per i dati. Gli alias vengono creati anche quando i puntatori puntano a variabili dichiarate. Nel frammento di codice seguente vengono illustrati entrambi i metodi di aliasing:


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



In un tipico programma C, è possibile specificare un albero binario usando la definizione seguente:


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



Più di un puntatore può accedere al contenuto di un nodo della struttura ad albero. Questa operazione è in genere corretta per le applicazioni non distribuite. Tuttavia, questo stile di programmazione genera un codice di supporto RPC più complesso. Gli stub client e server richiedono il codice aggiuntivo per gestire i dati e i puntatori. Il codice stub sottostante deve risolvere i diversi puntatori agli indirizzi e determinare la copia dei dati che rappresenta la versione più recente.

La quantità di elaborazione può essere ridotta se si garantisce che il puntatore sia l'unico modo in cui l'applicazione può accedere a tale area di memoria. Il puntatore può ancora avere molte delle funzionalità di un puntatore C. Ad esempio, può variare tra valori **null** e non **null** o rimanere invariati. Questa condizione è illustrata nell'esempio seguente. Il puntatore è **null** prima della chiamata e punta a una stringa valida dopo la chiamata:

![puntatore che cambia tra valori null e non null](images/prog-a01.png)

Per impostazione predefinita, il compilatore MIDL applica l' \[ attributo [univoco](/windows/desktop/Midl/unique) del \] puntatore a tutti i puntatori che non sono parametri. Questa impostazione predefinita può essere modificata con l' \[ [attributo \_ default del puntatore](/windows/desktop/Midl/pointer-default) \] .

Un puntatore univoco presenta le caratteristiche seguenti:

-   Il valore può essere **null**.
-   Può variare da **null** a non **null** durante la chiamata. Quando il valore viene modificato in un valore diverso da **null**, la nuova memoria viene allocata al momento della restituzione.
-   È possibile passare da un valore diverso da **null** a **null** durante la chiamata. Quando il valore viene modificato in **null**, l'applicazione è responsabile della liberazione della memoria.
-   Il valore può variare da un valore non **null** a un altro.
-   Non è possibile accedere alla risorsa di archiviazione a cui punta un puntatore univoco per qualsiasi altro puntatore o nome dell'operazione.
-   I dati restituiti vengono scritti nell'archiviazione esistente se il puntatore non ha il valore **null**.

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

In questo esempio il parametro *ACH* è un puntatore univoco ai dati di tipo carattere che vengono inviati a un server per l'elaborazione con la routine RemoteFn.

 

 