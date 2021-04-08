---
title: Uso dei servizi di serializzazione
description: MIDL genera uno stub di serializzazione per la procedura con gli attributi \ Encode \ e \ Decode \.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- RPC (Remote Procedure Call), attività, uso dei servizi di serializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047316"
---
# <a name="using-serialization-services"></a>Uso dei servizi di serializzazione

MIDL genera uno stub di serializzazione per la procedura con gli attributi \[ [**Encode**](/windows/desktop/Midl/encode) \] e \[ [**Decode**](/windows/desktop/Midl/decode) \] . Quando si chiama questa routine, si esegue una chiamata di serializzazione anziché una chiamata remota. Viene eseguito il marshalling o l'unmarshalling degli argomenti della routine da un buffer nel modo consueto. Si avrà quindi il controllo completo dei buffer.

Al contrario, quando il programma esegue la serializzazione del tipo (un tipo è contrassegnato con attributi di serializzazione), MIDL genera routine per ridimensionare, codificare e decodificare oggetti di quel tipo. Per serializzare i dati, è necessario chiamare queste routine nel modo appropriato. La serializzazione del tipo è un'estensione Microsoft e, di conseguenza, non è disponibile quando si esegue la compilazione in modalità di compatibilità DCE ([**/OSF**](/windows/desktop/Midl/-osf)). Utilizzando gli attributi \[ [**Encode**](/windows/desktop/Midl/encode) \] e \[ [**Decode**](/windows/desktop/Midl/decode) \] come attributi di interfaccia, RPC applica la codifica a tutti i tipi e routine definiti nel file IDL.

È necessario fornire buffer allineati in modo adeguato quando si utilizzano i servizi di serializzazione. L'inizio del buffer deve essere allineato a un indirizzo che è un multiplo di 8 o a 8 byte allineato. Per la serializzazione delle procedure, ogni chiamata di routine deve effettuare il marshalling o l'unmarshalling da una posizione del buffer a 8 byte allineata. Per la serializzazione dei tipi, il ridimensionamento, la codifica e la decodifica devono iniziare a una posizione allineata a 8 byte.

Un modo per garantire che i buffer siano allineati per l'applicazione consiste nel scrivere la funzione di [**\_ \_ allocazione utente MIDL**](/windows/desktop/Midl/midl-user-allocate-1) in modo da creare buffer allineati. Nell'esempio di codice riportato di seguito viene illustrato come eseguire questa operazione.


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



Nell'esempio seguente viene illustrata la funzione di [**MIDL \_ User \_ Free**](/windows/desktop/Midl/midl-user-free-1) corrispondente.


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



 

 