---
title: Puntatori completi
description: A differenza dei puntatori univoci, i puntatori completi supportano l'aliasing.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963187"
---
# <a name="full-pointers"></a>Puntatori completi

A differenza dei puntatori [univoci](unique-pointers.md) , i puntatori completi supportano l'aliasing. Ciò significa che più puntatori possono fare riferimento agli stessi dati, come illustrato nella figura seguente:

![due puntatori che fanno riferimento agli stessi dati](images/prog-a02.png)

Un puntatore completo presenta le caratteristiche seguenti:

-   Il valore può essere null.
-   Può variare da null a non null durante la chiamata. Quando il valore viene modificato in un valore diverso da null, lo stub client alloca la nuova memoria allocata al momento della restituzione. Il programma client deve liberare questa memoria prima di terminare.
-   È possibile passare da un valore diverso da null a null durante la chiamata. Quando il valore viene modificato in null, l'applicazione è responsabile della liberazione della memoria.
-   Il valore può variare da un valore non null a un altro.
-   È possibile accedere all'archiviazione a cui punta un puntatore completo tramite un altro puntatore o nome nell'operazione.
-   I dati restituiti vengono scritti nell'archiviazione esistente se il puntatore non ha il valore null.

Usare l' \[ attributo [**ptr**](/windows/desktop/Midl/ptr) \] per specificare un puntatore completo, come illustrato nell'esempio seguente:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

In questo esempio i parametri *ptrName1* e *ptrName2* sono definiti come puntatori completi a una stringa. È possibile che entrambi i puntatori puntino allo stesso indirizzo di memoria contenente una singola stringa.

\[**ptr** \] è obbligatorio quando si fornisce supporto per l'aliasing. Tuttavia, poiché richiede la maggior parte dell'elaborazione di tutti i puntatori disponibili in RPC, non è consigliabile per la maggior parte delle applicazioni.

 

 