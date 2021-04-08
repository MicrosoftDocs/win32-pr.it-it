---
title: Problemi di compressione del compilatore C
description: I livelli di compressione influiscono sul layout di memoria dei tipi sia per MIDL che per il compilatore Microsoft C/C++ nello stesso modo.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL compilatore MIDL, problemi di compressione del compilatore C
- creazione di pacchetti MIDL
- MIDL layout di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872453"
---
# <a name="c-compiler-packing-issues"></a>Problemi di compressione del compilatore C

I livelli di compressione influiscono sul layout di memoria dei tipi sia per MIDL che per il compilatore Microsoft C/C++ nello stesso modo. Negli ambienti di compilazione Microsoft, ad esempio l'ambiente di compilazione definito da VC + + o Platform Software Development Kit (SDK), il livello di compressione predefinito per i compilatori MIDL e C/C++ è lo stesso. il livello di compressione predefinito per gli ambienti di compilazione Windows a 32 bit e a 64 bit è 8.

## <a name="natural-alignment"></a>Allineamento naturale

Per i tipi in memoria, l'allineamento predefinito corrisponde al relativo allineamento naturale.

-   Un tipo di base, ad esempio short, float e \_ \_ Int64, e un puntatore è allineato naturalmente se la relativa rappresentazione inizia in corrispondenza di un indirizzo di modulo di dimensioni. Tutti i tipi di base attualmente supportati hanno dimensioni pari a 1, 2, 4 o 8. I puntatori hanno una dimensione di 4 negli ambienti a 32 bit e 8 negli ambienti a 64 bit.
-   Un tipo composto viene allineato naturalmente se ogni componente è allineato in modo naturale rispetto all'inizio del tipo e se non sono presenti gap superflui (riempimento) tra i componenti. I componenti composti, ad esempio i campi o gli elementi, vengono ricorsi al puntatore o ai componenti del tipo di base.

Una regola semplice che consente di ricordare questo comportamento è che l'allineamento naturale di un tipo è uguale agli allineamenti principali dei relativi componenti.

Esiste una connessione tra l'allineamento e le dimensioni della memoria di un tipo in linguaggi come C o C++ e IDL come espresso dall'operatore **sizeof ()**. La dimensione è un multiplo dell'allineamento (il multiplo minimo si estende sul tipo). Segue la rappresentazione di una matrice in memoria.

L'allineamento naturale è importante perché l'accesso a dati non allineati può causare un'eccezione in alcuni sistemi. I dati possono essere contrassegnati per una manipolazione sicura se non allineati, ma in genere comportano una riduzione della velocità che può essere sostanziale su alcune piattaforme.

> [!Note]  
> In memoria, gli oggetti di tipo con un allineamento naturale di *n* sono sicuramente allineati correttamente quando vengono posizionati su indirizzi che sono un multiplo di *n*.

 

## <a name="packing-versus-alignment"></a>Compressione rispetto all'allineamento

Se si specifica un livello di compressione maggiore di quello naturale di un tipo, l'allineamento del tipo non viene modificato. Se si specifica un livello di compressione inferiore a quello naturale, viene ridotto l'allineamento del tipo al livello di compressione. Di conseguenza, i tipi compressi possono essere inseriti in memoria negli indirizzi che sono un multiplo del livello di compressione, ovvero l'allineamento ridotto, senza causare errori di allineamento. Questa operazione ha effetto sia sui tipi semplici che sui tipi di componenti. Per i tipi composti, il layout interno del tipo potrebbe essere influenzato, in quanto l'allineamento ridotto dei componenti potrebbe modificare la dimensione della spaziatura interna necessaria per l'allineamento corretto dei componenti, riducendo così le dimensioni del tipo.

Una regola semplice che consente di ricordare questo comportamento è che il nuovo allineamento di un tipo compresso è il più piccolo del livello di compressione e il relativo allineamento naturale. Le dimensioni del tipo sono un multiplo del nuovo allineamento. L'operatore **sizeof ()** restituisce le dimensioni ridotte per i tipi compressi.

Ad esempio, con il livello di compressione 2 un Long viene allineato a 2 e pertanto può essere inserito in qualsiasi indirizzo, non solo negli indirizzi che sono un multiplo di 4 come nel caso dell'allineamento naturale. Una struttura con un valore short e Long, compresso su 2, non necessita del gap interno tra la breve e la lunghezza seguente necessaria per l'allineamento naturale; di conseguenza, non solo la struttura è ora allineata a 2, ma anche la sua dimensione è ridotta da 8 a 6.

Si consideri ad esempio un tipo composto costituito da un carattere a 1 byte, un numero intero di 4 byte e un carattere a 1 byte:

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

Questa struttura è naturalmente allineata a 4 e ha una dimensione naturale di 12.

Per il livello di compressione 4 o superiore, la struttura **struct** è allineata a 4 ed `sizeof(struct mystructtype)` è uguale a 12. La struttura verrà allineata in modo non corretto se si trova in memoria in un indirizzo che non è un multiplo di 4.

Per il livello di compressione 2, la struttura è allineata a 2 e la relativa dimensione è 8. La struttura compressa con livello 2 sarà allineata in modo non corretto se si trova in memoria in un indirizzo che non è un multiplo di 2.

Per il livello di compressione 1, la struttura è allineata a 1 e la relativa dimensione è 6. La struttura compressa con livello 1 può essere posizionata ovunque senza causare un errore di allineamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[/ZP](./-zp.md)
</dt> <dt>

[/Pack](./-pack.md)
</dt> </dl>

 

 