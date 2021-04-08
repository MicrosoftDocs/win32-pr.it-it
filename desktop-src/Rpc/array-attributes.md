---
title: Attributi di matrice
description: Esiste una relazione di chiusura tra matrici e puntatori nel linguaggio C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729434"
---
# <a name="array-attributes"></a>Attributi di matrice

Esiste una relazione di chiusura tra matrici e puntatori nel linguaggio C. Quando viene passato come parametro a una funzione, un nome di matrice viene considerato come un puntatore al primo elemento della matrice, come illustrato nell'esempio seguente:


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



In una chiamata locale è possibile usare il parametro pointer per procedere alla memoria ed esaminare il contenuto di altri indirizzi:


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



Quando un client passa un puntatore a una procedura remota, lo stub del client trasmette sia il puntatore che i dati a cui punta. A meno che il puntatore non sia limitato ai dati corrispondenti, tutta la memoria del client deve essere trasmessa con ogni chiamata remota. Applicando la tipizzazione forte nella definizione di interfaccia, MIDL limita l'elaborazione del client-Stub ai dati che corrispondono al puntatore specificato.

La dimensione della matrice e l'intervallo di elementi della matrice trasmessi al computer remoto possono essere costanti o variabili. Quando questi valori sono variabili e pertanto determinati in fase di esecuzione, è necessario utilizzare gli attributi nel file IDL per specificare il numero di elementi di matrice da trasmettere. Gli attributi MIDL seguenti supportano i limiti della matrice.



| Attributo                             | Descrizione                                             | Predefinito |
|---------------------------------------|---------------------------------------------------------|---------|
| \[il [ **primo \_ è**](/windows/desktop/Midl/first-is)\]   | Indice del primo elemento della matrice trasmesso.           | 0       |
| \[[ **ultimo \_ è**](/windows/desktop/Midl/last-is)\]     | Indice dell'ultimo elemento della matrice trasmesso.            | \-      |
| \[[ **lunghezza \_**](/windows/desktop/Midl/length-is)\] | Numero totale di elementi della matrice trasmessi.             | \-      |
| \[[ **Max \_ è**](/windows/desktop/Midl/max-is)\]       | Valore di indice di matrice valido più alto.                        | \-      |
| \[[ **Min \_ è**](/windows/desktop/Midl/min-is)\]       | Valore di indice di matrice valido più basso.                         | 0       |
| \[[ **dimensioni \_**](/windows/desktop/Midl/size-is)\]     | Numero totale di elementi della matrice allocati per la matrice. | \-      |



 

> [!Note]  
> L'attributo **Min \_ is** non è implementato in RPC. L'indice di matrice minimo viene sempre considerato come zero.

 

 

 