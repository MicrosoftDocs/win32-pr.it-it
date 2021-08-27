---
description: Nelle applicazioni Winsock un descrittore di socket non è un descrittore di file e deve essere usato con le funzioni winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Tipo di dati Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a95f890a14f68a0422ec91d31cb09735e2c85ab15cad52f9bd40499cee1167c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121241"
---
# <a name="socket-data-type"></a>Tipo di dati Socket

Nelle applicazioni Winsock un descrittore di socket non è un descrittore di file e deve essere usato con le funzioni winsock.

In UNIX, un descrittore di socket è rappresentato da un descrittore di file standard. Di conseguenza, un descrittore di socket in UNIX può essere passato a una qualsiasi delle funzioni di I/O di file standard ,ad esempio lettura e scrittura.

Inoltre, tutti gli handle in UNIX, inclusi gli handle di socket, sono numeri interi piccoli e non negativi e alcune applicazioni presunzione che ciò sia vero.

Windows Gli handle di socket non hanno restrizioni, a parte il fatto che il valore INVALID \_ SOCKET non è un socket valido. Gli handle di socket possono assumere qualsiasi valore compreso nell'intervallo da 0 a INVALID \_ SOCKET-1.

Poiché il tipo **SOCKET** è senza segno, la compilazione di codice sorgente esistente da, ad esempio, in un ambiente UNIX può causare la visualizzazione di avvisi del compilatore relativi a tipi di dati firmati/non firmati non corrispondenti.

Ciò significa, ad esempio, che il controllo degli errori quando le funzioni [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) restituiscono non deve essere eseguito confrontando il valore restituito con -1 o verificando se il valore è negativo (approcci comuni e legali in UNIX). Al contrario, un'applicazione deve usare la costante manifesto INVALID SOCKET come definito nel file di \_ *intestazione Winsock2.h.* Esempio:

Stile di UNIX BSD tipico


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



Stile preferito


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Porting di applicazioni socket in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Considerazioni sulla programmazione winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



