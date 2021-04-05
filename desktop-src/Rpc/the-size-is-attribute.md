---
title: Attributo size_is
description: L'attributo \ size \_ is \ è associato a una costante Integer, un'espressione o una variabile che specifica la dimensione di allocazione della matrice.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872629"
---
# <a name="the-size_is-attribute"></a>La \[ dimensione \_ è \] attribute

L' \[ attributo [size \_ è](/windows/desktop/Midl/size-is) \] associato a una costante Integer, un'espressione o una variabile che specifica la dimensione di allocazione della matrice. Si consideri una matrice di caratteri la cui lunghezza è determinata dall'input dell'utente:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> L'asterisco ( \* ) che contrassegna il segnaposto per la dimensione della matrice di variabili è facoltativo.

 

Lo stub del server deve allocare memoria nel server che corrisponde alla memoria del client per il parametro. La variabile che specifica la dimensione deve essere sempre almeno un parametro \[ [in](/windows/desktop/Midl/in) \] . L'attributo Directional è obbligatorio, **\[ in \]** modo che il valore Size venga definito alla voce dello stub del server. Questo valore di dimensione fornisce informazioni che lo stub del server richiede per allocare la memoria.

Il parametro size può essere anche \[ in [uscita](/windows/desktop/Midl/out-idl) \] . Questa operazione è utile se, ad esempio, l'array inviato dal client non è sufficientemente grande per i dati che il server deve archiviare. È possibile utilizzare un parametro **\[ in, \] out** size per restituire le dimensioni richieste al programma client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Più livelli di puntatori](multiple-levels-of-pointers.md)
</dt> </dl>

 

 