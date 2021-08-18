---
title: Uso dei servizi di serializzazione
description: MIDL genera uno stub di serializzazione per la procedura con gli attributi \ encode\ e \ decode\ .
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- Chiamata di procedura remota RPC , attività, uso dei servizi di serializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be20d513bdb74eca316b022dd8536e8988e32e93099981cc77830035048e55e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010629"
---
# <a name="using-serialization-services"></a>Uso dei servizi di serializzazione

MIDL genera uno stub di serializzazione per la procedura con gli attributi \[ [**di codifica**](/windows/desktop/Midl/encode) \] e \[ [**decodifica**](/windows/desktop/Midl/decode) \] . Quando si chiama questa routine, si esegue una chiamata di serializzazione anziché una chiamata remota. Il marshalling o l'annullamento del marshalling degli argomenti della routine da un buffer viene eseguito nel modo consueto. Si ha quindi il controllo completo dei buffer.

Al contrario, quando il programma esegue la serializzazione dei tipi (un tipo è etichettato con attributi di serializzazione), MIDL genera routine per ridimensionare, codificare e decodificare oggetti di quel tipo. Per serializzare i dati, è necessario chiamare queste routine nel modo appropriato. La serializzazione dei tipi è un'estensione Microsoft e, di conseguenza, non è disponibile quando si esegue la compilazione in modalità di compatibilità DCE ([**/osf**](/windows/desktop/Midl/-osf)). Usando gli attributi di codifica e decodifica come attributi di interfaccia, RPC applica la codifica a tutti i tipi e \[ [](/windows/desktop/Midl/encode) \] routine definiti \[ [](/windows/desktop/Midl/decode) \] nel file IDL.

Quando si usano i servizi di serializzazione, è necessario fornire buffer allineati in modo adeguato. L'inizio del buffer deve essere allineato in corrispondenza di un indirizzo multiplo di 8 o 8 byte allineato. Per la serializzazione di routine, ogni chiamata di routine deve effettuare il marshalling in o annullare il marshalling da una posizione del buffer allineata a 8 byte. Per la serializzazione del tipo, il ridimensionamento, la codifica e la decodifica devono iniziare da una posizione allineata a 8 byte.

Un modo per garantire che i buffer dell'applicazione siano allineati è scrivere la funzione di allocazione utente [**midl \_ \_**](/windows/desktop/Midl/midl-user-allocate-1) in modo che crei buffer allineati. L'esempio di codice seguente illustra come eseguire questa operazione.


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



Nell'esempio seguente viene illustrata la funzione [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1) corrispondente.


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 