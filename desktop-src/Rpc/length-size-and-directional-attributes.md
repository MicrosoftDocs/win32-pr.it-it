---
title: Attributi di lunghezza, dimensione e direzionali
description: Nel passaggio di matrici tra il client e il server, gli attributi correlati alle dimensioni \ max is\ e \ size is\ determinano quanti elementi della matrice vengono allocati dal \_ \_ server stub.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e91424a93a53fe710c945011d19f8f97dc0f65e4899bc3305be5725d5a08e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020132"
---
# <a name="length-size-and-directional-attributes"></a>Attributi di lunghezza, dimensione e direzionali

Nel passaggio di matrici tra il client e il server, il numero massimo di attributi correlati alle dimensioni è e size determina il numero di elementi della matrice allocati dal \[ [**\_**](/windows/desktop/Midl/max-is) \] server \[ [**\_**](/windows/desktop/Midl/size-is) \] stub. La lunghezza degli attributi correlati alla lunghezza è , la prima è e l'ultima è determinare il numero di elementi trasmessi sia \[ [**\_**](/windows/desktop/Midl/length-is)al server \] che al \[ [**\_**](/windows/desktop/Midl/first-is) \] \[ [**\_**](/windows/desktop/Midl/last-is) \] client.

È possibile applicare attributi direzionali diversi ai parametri. Tuttavia, alcune combinazioni di attributi direzionali possono causare errori. Si supponga, ad esempio, di scrivere un'interfaccia che specifica una routine con due parametri, una matrice e la lunghezza trasmessa della matrice. Il termine *dir \_ attr* si riferisce all'attributo direzionale applicato al parametro come:

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

Il comportamento del compilatore MIDL per ogni combinazione di attributi direzionali è descritto nella tabella seguente.



| Array                                          | Parametro length                               | Azioni stub durante la chiamata da client a server                                                                                                                                                                                                                          | Azioni stub al ritorno da server a client                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**Pollici**](/windows/desktop/Midl/in)\]                          | \[[**Pollici**](/windows/desktop/Midl/in)\]                          | Trasmettere la lunghezza e il numero di elementi indicati dal parametro .                                                                                                                                                                                              | Nessun dato trasmesso.                                                                                                                                                                                                 |
| \[[**Pollici**](/windows/desktop/Midl/in)\]                          | \[[**Cambio**](/windows/desktop/Midl/out-idl)\]                    | Non legale; Errore del compilatore MIDL.                                                                                                                                                                                                                                         | Non legale; Errore del compilatore MIDL.                                                                                                                                                                                      |
| \[[**Pollici**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Trasmettere la lunghezza e il numero di elementi indicati dal parametro length.                                                                                                                                                                                       | Trasmettere solo la lunghezza.                                                                                                                                                                                            |
| \[[**Cambio**](/windows/desktop/Midl/out-idl)\]                    | \[[**Pollici**](/windows/desktop/Midl/in)\]                          | Trasmettere la lunghezza.<br/> Se le dimensioni della matrice sono fisse, allocare le dimensioni della matrice nel server, ma non trasmettere elementi.<br/> Se la dimensione della matrice non è associata, non è consentita: errore del compilatore MIDL.<br/>                                                              | Trasmettere il numero di elementi indicato dalla lunghezza.<br/> Si noti che la lunghezza può essere modificata e può avere un valore diverso da quello nel client. Non trasmettere la lunghezza.<br/>          |
| \[[**Cambio**](/windows/desktop/Midl/out-idl)\]                    | \[[**Cambio**](/windows/desktop/Midl/out-idl)\]                    | Allocare spazio per il parametro length nel server, ma non trasmette il parametro. Se le dimensioni della matrice sono fisse, allocare le dimensioni della matrice nel server, ma non trasmettere elementi.<br/> Se le dimensioni della matrice non sono fisse, non sono consentite: errore del compilatore MIDL.<br/> | Trasmettere la lunghezza e il numero di elementi indicati dalla lunghezza impostata dall'applicazione server.                                                                                                             |
| \[[**Cambio**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Trasmettere il parametro length. Se la dimensione della matrice è associata, allocare le dimensioni della matrice nel server, ma non trasmettere elementi.<br/> Se la dimensione della matrice non è associata, non è consentita: errore del compilatore MIDL.<br/>                                                           | Trasmettere la lunghezza. Trasmettere il numero di elementi della matrice indicati dalla lunghezza.<br/>                                                                                                                       |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**Pollici**](/windows/desktop/Midl/in)\]                          | Trasmettere la lunghezza e il numero di elementi indicati dal parametro .                                                                                                                                                                                              | Non trasmettere la lunghezza. Trasmettere il numero di elementi indicato dalla lunghezza.<br/> Si noti che la lunghezza può essere modificata e può avere un valore diverso da quello originale nel client.<br/> |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**Cambio**](/windows/desktop/Midl/out-idl)\]                    | Non legale; Errore del compilatore MIDL.                                                                                                                                                                                                                                         | Non legale; Errore del compilatore MIDL.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Trasmettere la lunghezza e il numero di elementi indicati dal parametro .                                                                                                                                                                                              | Trasmettere la lunghezza e il numero di elementi indicati dal parametro .                                                                                                                                           |



 

In generale, è consigliabile non modificare i parametri di lunghezza o dimensione sul lato server. Se si modifica il parametro length, è possibile usare la memoria orfana. Per altre informazioni, vedere [Orfano della memoria.](memory-orphaning.md)

 

