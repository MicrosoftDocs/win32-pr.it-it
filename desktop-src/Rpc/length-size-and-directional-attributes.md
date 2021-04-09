---
title: Attributi di lunghezza, dimensioni e direzionali
description: Per passare le matrici tra il client e il server, gli attributi relativi alle dimensioni \ Max \_ sono \ e \ size \_ è \ determinare il numero di elementi della matrice allocati dallo stub del server.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ffbf1ac75ad82a89e258ab595590fce2190b9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729306"
---
# <a name="length-size-and-directional-attributes"></a>Attributi di lunghezza, dimensioni e direzionali

Nel passaggio di matrici tra il client e il server, gli attributi relativi alle dimensioni \[ [**Max \_ è**](/windows/desktop/Midl/max-is) \] e \[ [**size \_**](/windows/desktop/Midl/size-is) \] determinano il numero di elementi di matrice allocati dallo stub del server. La lunghezza degli attributi correlati alla lunghezza \[ [**\_ è**](/windows/desktop/Midl/length-is) \] , \[ [**First \_ è**](/windows/desktop/Midl/first-is) \] e \[ [**Last \_ è**](/windows/desktop/Midl/last-is) \] determinare il numero di elementi trasmessi sia al server che al client.

È possibile applicare attributi direzionali diversi ai parametri. Tuttavia, alcune combinazioni di attributi direzionali possono causare errori. Si supponga, ad esempio, di scrivere un'interfaccia che specifichi una routine con due parametri, una matrice e la lunghezza trasmessa della matrice. Il termine *dir \_ attr* si riferisce all'attributo direzionale applicato al parametro come:

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

Il comportamento del compilatore MIDL per ogni combinazione di attributi direzionali è descritto nella tabella seguente.



| Array                                          | Parametro length                               | Azioni Stub durante la chiamata dal client al server                                                                                                                                                                                                                          | Azioni Stub al ritorno da server a client                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**in**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in)\]                          | Trasmettere la lunghezza e il numero di elementi indicati dal parametro.                                                                                                                                                                                              | Nessun dato trasmesso.                                                                                                                                                                                                 |
| \[[**in**](/windows/desktop/Midl/in)\]                          | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Non valido; Errore del compilatore MIDL.                                                                                                                                                                                                                                         | Non valido; Errore del compilatore MIDL.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in) [ **uscita**](/windows/desktop/Midl/out-idl)\] | Trasmettere la lunghezza e il numero di elementi indicati dal parametro length.                                                                                                                                                                                       | Trasmettere solo la lunghezza.                                                                                                                                                                                            |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in)\]                          | Trasmettere la lunghezza.<br/> Se le dimensioni della matrice sono fisse, allocare le dimensioni della matrice sul server, ma non trasmettere alcun elemento.<br/> Se la dimensione della matrice non è associata, non valida: errore del compilatore MIDL.<br/>                                                              | Trasmette il numero di elementi indicato dalla lunghezza.<br/> Si noti che la lunghezza può essere modificata e può avere un valore diverso dal valore del client. Non trasmettere la lunghezza.<br/>          |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Allocare spazio per il parametro length sul server ma non trasmettere il parametro. Se le dimensioni della matrice sono fisse, allocare le dimensioni della matrice sul server, ma non trasmettere alcun elemento.<br/> Se la dimensione della matrice non è fissa, non valida: errore del compilatore MIDL.<br/> | Trasmettere la lunghezza e il numero di elementi indicati dalla lunghezza impostata dall'applicazione server.                                                                                                             |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in) [ **uscita**](/windows/desktop/Midl/out-idl)\] | Trasmettere il parametro length. Se la dimensione della matrice è associata, allocare la dimensione della matrice sul server, ma non trasmettere alcun elemento.<br/> Se la dimensione della matrice non è associata, non valida: errore del compilatore MIDL.<br/>                                                           | Trasmettere la lunghezza. Trasmette il numero di elementi di matrice indicati dalla lunghezza.<br/>                                                                                                                       |
| \[[**in**](/windows/desktop/Midl/in) [ **uscita**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in)\]                          | Trasmettere la lunghezza e il numero di elementi indicati dal parametro.                                                                                                                                                                                              | Non trasmettere la lunghezza. Trasmette il numero di elementi indicato dalla lunghezza.<br/> Si noti che la lunghezza può essere modificata e può avere un valore diverso rispetto al valore originale nel client.<br/> |
| \[[**in**](/windows/desktop/Midl/in) [ **uscita**](/windows/desktop/Midl/out-idl)\] | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Non valido; Errore del compilatore MIDL.                                                                                                                                                                                                                                         | Non valido; Errore del compilatore MIDL.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in) [ **uscita**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in) [ **uscita**](/windows/desktop/Midl/out-idl)\] | Trasmettere la lunghezza e il numero di elementi indicati dal parametro.                                                                                                                                                                                              | Trasmettere la lunghezza e il numero di elementi indicati dal parametro.                                                                                                                                           |



 

In generale, non è consigliabile modificare i parametri length o size sul lato server. Se si modifica il parametro length, è possibile che la memoria sia orfana. Per ulteriori informazioni, vedere [orfano di memoria](memory-orphaning.md).

 

