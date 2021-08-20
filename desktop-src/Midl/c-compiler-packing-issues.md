---
title: Problemi di creazione di un pacchetto del compilatore C
description: I livelli di creazione di un pacchetto influiscono nello stesso modo sul layout di memoria dei tipi sia per MIDL che per il compilatore Microsoft C/C++.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL compiler MIDL , C-compiler packing issues
- creazione di un pacchetto MIDL
- layout di memoria MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d355214c7f3222d67fd7673de4f9d32d19b4c885e8f97143c80df7b98bc0e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807894"
---
# <a name="c-compiler-packing-issues"></a>Problemi di creazione di un pacchetto del compilatore C

I livelli di creazione di un pacchetto influiscono nello stesso modo sul layout di memoria dei tipi sia per MIDL che per il compilatore Microsoft C/C++. Negli ambienti di compilazione Microsoft, ad esempio l'ambiente di compilazione definito da VC++ o Platform Software Development Kit (SDK), il livello di creazione pacchetti predefinito per i compilatori MIDL e C/C++ è lo stesso; il livello di packing predefinito per gli ambienti di compilazione Windows a 32 bit e a 64 bit è 8.

## <a name="natural-alignment"></a>Allineamento naturale

Per i tipi in memoria, l'allineamento predefinito corrisponde all'allineamento naturale.

-   Un tipo di base, ad esempio short, float e \_ int64, e un puntatore viene allineato in modo naturale se la relativa rappresentazione inizia in corrispondenza di un indirizzo di \_ dimensioni modulo. Tutti i tipi di base attualmente supportati hanno dimensioni di 1, 2, 4 o 8. Le dimensioni dei puntatori sono 4 in ambienti a 32 bit e 8 in ambienti a 64 bit.
-   Un tipo composto è allineato naturalmente se ognuno dei relativi componenti è allineato naturalmente rispetto all'inizio del tipo e se non sono presenti spazi non necessari (riempimento) tra i componenti. I componenti composti, ad esempio campi o elementi, vengono ricorsi ai componenti del puntatore o del tipo di base.

Una regola semplice per ricordare questo comportamento è che l'allineamento naturale di un tipo è uguale agli allineamenti principali dei componenti.

Esiste una connessione tra allineamento e dimensioni della memoria di un tipo in linguaggi come C o C++ e IDL come espresso dall'operatore **sizeof().** La dimensione è un multiplo dell'allineamento (il multiplo minimo che si estende sul tipo). Ciò è seguito da una rappresentazione di matrice in memoria.

L'allineamento naturale è importante perché l'accesso a dati non allineati può causare un'eccezione in alcuni sistemi. I dati possono essere contrassegnati per una manipolazione sicura quando non allineati in modo non allineato, ma in genere ciò comporta una riduzione della velocità che può essere sostanziale in alcune piattaforme.

> [!Note]  
> In memoria, gli oggetti di tipi con un allineamento naturale di *n* sono garantiti per essere allineati correttamente quando posizionati in corrispondenza di indirizzi che sono un multiplo di *n*.

 

## <a name="packing-versus-alignment"></a>Confronto tra allineamento e tabulazione

Se si specifica un livello di tabulazione maggiore dell'allineamento naturale di un tipo, l'allineamento del tipo non viene modificato. Se si specifica un livello di packing inferiore all'allineamento naturale, l'allineamento del tipo al livello di packing viene ridotto. Di conseguenza, i tipi di tipo packed possono essere inseriti in memoria in indirizzi che sono un multiplo del livello di packing (allineamento ridotto) senza causare un disallineamento. Questo influisce sia sui tipi semplici che sui tipi di componente. Per i tipi composti, il layout interno del tipo può essere influenzato, perché l'allineamento ridotto dei componenti può modificare le dimensioni della spaziatura interna necessaria per l'allineamento corretto dei componenti, riducendo così le dimensioni del tipo.

Una regola semplice per ricordare questo comportamento è che il nuovo allineamento di un tipo di tipo packed è il più piccolo del livello di packing e il relativo allineamento naturale. La dimensione del tipo è un multiplo del nuovo allineamento. **L'operatore sizeof()** restituisce la dimensione ridotta per i tipi di cui è stato fatto il pacchetto.

Ad esempio, con il livello di packing 2 un valore long viene allineato a 2 e pertanto può essere posizionato in qualsiasi indirizzo pari, non solo in corrispondenza degli indirizzi che sono un multiplo di 4, come nel caso dell'allineamento naturale. Una struttura con una struttura breve e una lunga, imballata in corrispondenza di 2, non richiede il divario interno tra il breve e il seguente lungo necessario per l'allineamento naturale; Di conseguenza, non solo la struttura è ora allineata a 2, ma anche le dimensioni sono ridotte da 8 a 6.

Si consideri ad esempio un tipo composto costituito da un carattere a 1 byte, da un numero intero di 4 byte e da un carattere a 1 byte:

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

Questa struttura è naturalmente allineata a 4 e ha dimensioni naturali di 12.

Per il livello di creazione di un pacchetto 4 o superiore, la struttura **mystruct** è allineata a 4 ed `sizeof(struct mystructtype)` è uguale a 12. La struttura non sarà allineata se si trova in memoria in un indirizzo che non è un multiplo di 4.

Per il livello di packing 2, la struttura è allineata a 2 e le relative dimensioni sono 8. La struttura con livello 2 non sarà allineata se si trova in memoria in un indirizzo che non è un multiplo di 2.

Per il livello di packing 1, la struttura è allineata a 1 e le relative dimensioni sono 6. La struttura con livello 1 può essere posizionata ovunque senza causare un errore di disallineamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[/Zp](./-zp.md)
</dt> <dt>

[/pack](./-pack.md)
</dt> </dl>

 

 