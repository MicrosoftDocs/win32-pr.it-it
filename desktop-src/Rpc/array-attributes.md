---
title: Attributi di matrice
description: Esiste una stretta relazione tra matrici e puntatori nel linguaggio C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba7bdaa08352a96987066313d4db074872f28b71ec0be0856a32522a849029c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073521"
---
# <a name="array-attributes"></a>Attributi di matrice

Esiste una stretta relazione tra matrici e puntatori nel linguaggio C. Quando viene passato come parametro a una funzione, un nome di matrice viene considerato come un puntatore al primo elemento della matrice, come illustrato nell'esempio seguente:


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



In una chiamata locale è possibile usare il parametro pointer per scorrere la memoria ed esaminare il contenuto di altri indirizzi:


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



Quando un client passa un puntatore a una procedura remota, lo stub del client trasmette sia il puntatore che i dati a cui punta. A meno che il puntatore non sia limitato ai dati corrispondenti, tutta la memoria del client deve essere trasmessa con ogni chiamata remota. Tramite l'applicazione della tipizzazione forte nella definizione dell'interfaccia, MIDL limita l'elaborazione dello stub client ai dati che corrispondono al puntatore specificato.

Le dimensioni della matrice e l'intervallo di elementi della matrice trasmessi al computer remoto possono essere costanti o variabili. Quando questi valori sono variabili e quindi determinati in fase di esecuzione, è necessario usare gli attributi nel file IDL per specificare il numero di elementi della matrice da trasmettere. Gli attributi MIDL seguenti supportano i limiti di matrice.



| Attributo                             | Descrizione                                             | Predefinito |
|---------------------------------------|---------------------------------------------------------|---------|
| \[[ **first \_ è**](/windows/desktop/Midl/first-is)\]   | Indice del primo elemento della matrice trasmesso.           | 0       |
| \[[ **last \_ is**](/windows/desktop/Midl/last-is)\]     | Indice dell'ultimo elemento della matrice trasmesso.            | \-      |
| \[[ **length \_ è**](/windows/desktop/Midl/length-is)\] | Numero totale di elementi della matrice trasmessi.             | \-      |
| \[[ **max \_ is**](/windows/desktop/Midl/max-is)\]       | Valore massimo di indice di matrice valido.                        | \-      |
| \[[ **min \_ is**](/windows/desktop/Midl/min-is)\]       | Valore di indice della matrice valido più basso.                         | 0       |
| \[[ **size \_ è**](/windows/desktop/Midl/size-is)\]     | Numero totale di elementi della matrice allocati per la matrice. | \-      |



 

> [!Note]  
> **\_ L'attributo min is** non è implementato in RPC. L'indice minimo della matrice viene sempre considerato come zero.

 

 

 